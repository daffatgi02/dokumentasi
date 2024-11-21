# kWh Meter Data Logging API Documentation

## Endpoint
`POST /addData/:floor`
ex: `POST /addData/lantai1`
ex: `POST /addData/lantai1_annex`
### Parameters
- `floor` (URL parameter, required): Floor identifier 
  - Accepted values:
    - `lantai1`
    - `lantai1_annex`
    - `lantai2`
    - `lantai2_annex`
    - `lantai3`
    - `lantai3_annex`
    - `lantai4`
    - `lantai5`
    - `lantai6`
    - `lantai7`
    - `lantai8`
    - `lantaiEksternal`
    - `lantaiGround`

### Request Body (JSON)
| Field         | Type   |
|---------------|--------|
| no_kWh_Meter  | Number |
| v_avg         | String | 
| I_avg         | String |
| PF_avg        | String |
| kVA           | String |
| kW            | String |
| kVArh         | String |
| freq          | String |
| v_l1          | String |
| v_l2          | String | 
| v_l3          | String |
| v_12          | String |
| v_23          | String |
| v_31          | String |
| I_A1          | String |
| I_A2          | String |
| I_A3          | String |

### Responses

#### Success Response (200 OK)
```json
{
    "success": true,
    "message": "Data successfully inserted into kWh meter logs for {floor}",
    "data": {
        "no_kWh_Meter": number,
        "nama_kWh_Meter": string,
        "freq": string,
        "v_l1": string,
        "v_l2": string,
        "v_l3": string,
        "v_12": string,
        "v_23": string,
        "v_31": string,
        "I_A1": string,
        "I_A2": string,
        "I_A3": string,
        "log_waktu": timestamp,
        "v_avg": string,
        "I_avg": string,
        "kVA": string,
        "kW": string,
        "PF_avg": string,
        "kVArh": string
    }
}
```

