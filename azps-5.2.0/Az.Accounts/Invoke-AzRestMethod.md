---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/invoke-azrestmethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Invoke-AzRestMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Invoke-AzRestMethod.md
ms.openlocfilehash: f8475c7cead6159231314989d21430658128c01f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363901"
---
# <span data-ttu-id="ad599-101">Invoke-AzRestMethod</span><span class="sxs-lookup"><span data-stu-id="ad599-101">Invoke-AzRestMethod</span></span>

## <span data-ttu-id="ad599-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ad599-102">SYNOPSIS</span></span>
<span data-ttu-id="ad599-103">Costruire ed eseguire una richiesta HTTP solo all'endpoint di gestione delle risorse Azure</span><span class="sxs-lookup"><span data-stu-id="ad599-103">Construct and perform HTTP request to Azure resource management endpoint only</span></span>

## <span data-ttu-id="ad599-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ad599-104">SYNTAX</span></span>

### <span data-ttu-id="ad599-105">ByPath (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ad599-105">ByPath (Default)</span></span>
```
Invoke-AzRestMethod -Path <String> -Method <String> [-Payload <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad599-106">ByParameters</span><span class="sxs-lookup"><span data-stu-id="ad599-106">ByParameters</span></span>
```
Invoke-AzRestMethod [-SubscriptionId <String>] [-ResourceGroupName <String>] [-ResourceProviderName <String>]
 [-ResourceType <String[]>] [-Name <String[]>] -ApiVersion <String> -Method <String> [-Payload <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad599-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad599-107">DESCRIPTION</span></span>
<span data-ttu-id="ad599-108">Costruire ed eseguire una richiesta HTTP solo all'endpoint di gestione delle risorse Azure</span><span class="sxs-lookup"><span data-stu-id="ad599-108">Construct and perform HTTP request to Azure resource management endpoint only</span></span>

## <span data-ttu-id="ad599-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ad599-109">EXAMPLES</span></span>

### <span data-ttu-id="ad599-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ad599-110">Example 1</span></span>
```powershell
Invoke-AzRestMethod -Path "/subscriptions/{subscription}/resourcegroups/{resourcegroup}/providers/microsoft.operationalinsights/workspaces/{workspace}?api-version={API}" -Method GET

Headers    : {[Cache-Control, System.String[]], [Pragma, System.String[]], [x-ms-request-id, System.String[]], [Strict-Transport-Security, System.String[]]…}
Version    : 1.1
StatusCode : 200
Method     : GET
Content    : {
               "properties": {
                 "source": "Azure",
                 "customerId": "{customerId}",
                 "provisioningState": "Succeeded",
                 "sku": {
                   "name": "pergb2018",
                   "maxCapacityReservationLevel": 3000,
                   "lastSkuUpdate": "Mon, 25 May 2020 11:10:01 GMT"
                 },
                 "retentionInDays": 30,
                 "features": {
                   "legacy": 0,
                   "searchVersion": 1,
                   "enableLogAccessUsingOnlyResourcePermissions": true
                 },
                 "workspaceCapping": {
                   "dailyQuotaGb": -1.0,
                   "quotaNextResetTime": "Thu, 18 Jun 2020 05:00:00 GMT",
                   "dataIngestionStatus": "RespectQuota"
                 },
                 "enableFailover": false,
                 "publicNetworkAccessForIngestion": "Enabled",
                 "publicNetworkAccessForQuery": "Enabled",
                 "createdDate": "Mon, 25 May 2020 11:10:01 GMT",
                 "modifiedDate": "Mon, 25 May 2020 11:10:02 GMT"
               },
               "id": "/subscriptions/{subscription}/resourcegroups/{resourcegroup}/providers/microsoft.operationalinsights/workspaces/{workspace}",
               "name": "{workspace}",
               "type": "Microsoft.OperationalInsights/workspaces",
               "location": "eastasia",
               "tags": {}
             }
```

<span data-ttu-id="ad599-111">Ottenere l'area di lavoro analisi log per percorso</span><span class="sxs-lookup"><span data-stu-id="ad599-111">Get log analytics workspace by path</span></span>

## <span data-ttu-id="ad599-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ad599-112">PARAMETERS</span></span>

### <span data-ttu-id="ad599-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ad599-113">-ApiVersion</span></span>
<span data-ttu-id="ad599-114">Versione API</span><span class="sxs-lookup"><span data-stu-id="ad599-114">Api Version</span></span>

```yaml
Type: String
Parameter Sets: ByParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad599-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad599-115">-AsJob</span></span>
<span data-ttu-id="ad599-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ad599-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad599-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad599-117">-DefaultProfile</span></span>
<span data-ttu-id="ad599-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ad599-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad599-119">-Method</span><span class="sxs-lookup"><span data-stu-id="ad599-119">-Method</span></span>
<span data-ttu-id="ad599-120">Metodo http</span><span class="sxs-lookup"><span data-stu-id="ad599-120">Http Method</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: GET, POST, PUT, PATCH, DELETE

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad599-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="ad599-121">-Name</span></span>
<span data-ttu-id="ad599-122">elenco del nome della risorsa di destinazione</span><span class="sxs-lookup"><span data-stu-id="ad599-122">list of Target Resource Name</span></span>

```yaml
Type: String[]
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad599-123">-Path</span><span class="sxs-lookup"><span data-stu-id="ad599-123">-Path</span></span>
<span data-ttu-id="ad599-124">Percorso di destinazione</span><span class="sxs-lookup"><span data-stu-id="ad599-124">Target Path</span></span>

```yaml
Type: String
Parameter Sets: ByPath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad599-125">-Payload</span><span class="sxs-lookup"><span data-stu-id="ad599-125">-Payload</span></span>
<span data-ttu-id="ad599-126">Payload in formato JSON</span><span class="sxs-lookup"><span data-stu-id="ad599-126">JSON format payload</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad599-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad599-127">-ResourceGroupName</span></span>
<span data-ttu-id="ad599-128">Nome del gruppo di risorse di destinazione</span><span class="sxs-lookup"><span data-stu-id="ad599-128">Target Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad599-129">-ResourceProviderName</span><span class="sxs-lookup"><span data-stu-id="ad599-129">-ResourceProviderName</span></span>
<span data-ttu-id="ad599-130">Nome del provider di risorse di destinazione</span><span class="sxs-lookup"><span data-stu-id="ad599-130">Target Resource Provider Name</span></span>

```yaml
Type: String
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad599-131">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="ad599-131">-ResourceType</span></span>
<span data-ttu-id="ad599-132">Elenco di tipo di risorsa di destinazione</span><span class="sxs-lookup"><span data-stu-id="ad599-132">List of Target Resource Type</span></span>

```yaml
Type: String[]
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad599-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ad599-133">-SubscriptionId</span></span>
<span data-ttu-id="ad599-134">ID abbonamento di destinazione</span><span class="sxs-lookup"><span data-stu-id="ad599-134">Target Subscription Id</span></span>

```yaml
Type: String
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad599-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ad599-135">-Confirm</span></span>
<span data-ttu-id="ad599-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad599-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad599-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad599-137">-WhatIf</span></span>
<span data-ttu-id="ad599-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ad599-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad599-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ad599-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad599-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad599-140">CommonParameters</span></span>
<span data-ttu-id="ad599-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad599-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad599-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad599-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad599-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ad599-143">INPUTS</span></span>

### <span data-ttu-id="ad599-144">System. String</span><span class="sxs-lookup"><span data-stu-id="ad599-144">System.string</span></span>

## <span data-ttu-id="ad599-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ad599-145">OUTPUTS</span></span>

### <span data-ttu-id="ad599-146">Microsoft. Azure. Commands. profile. Models. PSHttpResponse</span><span class="sxs-lookup"><span data-stu-id="ad599-146">Microsoft.Azure.Commands.Profile.Models.PSHttpResponse</span></span>

## <span data-ttu-id="ad599-147">Note</span><span class="sxs-lookup"><span data-stu-id="ad599-147">NOTES</span></span>

## <span data-ttu-id="ad599-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ad599-148">RELATED LINKS</span></span>
