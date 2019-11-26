# 140SL-Final-Project


load("purchase.RData")
View(purchase)
load("ga.RData")
View(ga)
load("adwords.RData")
View(adwords)
codebook_purchase <- read_excel("codebook_final_v3.xlsx", 
                                sheet = "purchase.csv")
codebook_adwords <- read_excel("codebook_final_v3.xlsx", 
                               sheet = "adwords")
codebook_user <- read_excel("codebook_final_v3.xlsx", 
                            sheet = "User_Behavior(GA_DATA)")
View(codebook_user)

purchase %>% group_by(venue_state, venue_city) %>% count(sort = TRUE)

purchase %>% group_by(event_name) %>% count(sort = TRUE)

purchase %>% filter(event_name == "Beyonce - the formation world tour") %>%
  group_by(venue_state, venue_city) %>% count(sort = TRUE)

purchase %>% filter(event_name == "Dave Matthews Band") %>%
  group_by(venue_state, venue_city) %>% count(sort = TRUE)


purchase %>%  filter(la_event_type_cat != "PARKING") %>% group_by(la_event_type_cat, minor_cat_name, venue_state) %>% count(sort = TRUE)

purchase %>% group_by(la_event_type_cat) %>% count()

sum(purchase$venue_state == "CALIFORNIA") / length(purchase$venue_state == "CALIFORNIA")


purchase %>% group_by(event_name) %>% 
  summarise(total_tickets_purchased = sum(tickets_purchased_qty)) %>%
  arrange(desc(total_tickets_purchased))


ga %>% group_by(attraction_id) %>% count(sort = TRUE)
