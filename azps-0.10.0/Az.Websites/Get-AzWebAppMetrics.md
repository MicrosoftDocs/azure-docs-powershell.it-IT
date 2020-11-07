---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 513BE097-EB4A-4C49-9F7F-42A2BED09022
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppMetrics.md
ms.openlocfilehash: 9a3aeabc3eb38127b37ca4ab6a12975c51daea5b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861938"
---
# <span data-ttu-id="c5619-101">Get-AzWebAppMetrics</span><span class="sxs-lookup"><span data-stu-id="c5619-101">Get-AzWebAppMetrics</span></span>

## <span data-ttu-id="c5619-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c5619-102">SYNOPSIS</span></span>
<span data-ttu-id="c5619-103">Ottiene le metriche di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="c5619-103">Gets Azure Web App metrics.</span></span>

## <span data-ttu-id="c5619-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c5619-104">SYNTAX</span></span>

### <span data-ttu-id="c5619-105">S1</span><span class="sxs-lookup"><span data-stu-id="c5619-105">S1</span></span>
```
Get-AzWebAppMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5619-106">S2</span><span class="sxs-lookup"><span data-stu-id="c5619-106">S2</span></span>
```
Get-AzWebAppMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c5619-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c5619-107">DESCRIPTION</span></span>
<span data-ttu-id="c5619-108">Il **Get-AzWebAppMetrics** ottiene le metriche delle app Web.</span><span class="sxs-lookup"><span data-stu-id="c5619-108">The **Get-AzWebAppMetrics** gets Web App metrics.</span></span>

## <span data-ttu-id="c5619-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c5619-109">EXAMPLES</span></span>

### <span data-ttu-id="c5619-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c5619-110">Example 1</span></span>
```
PS C:\> Get-AzAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="c5619-111">Questo comando ottiene le richieste dell'app Web ContosoWebApp al minuto (PT1M-polling Time 1 minute) tra StartTime e EndTime</span><span class="sxs-lookup"><span data-stu-id="c5619-111">This command gets Requests of the Web App ContosoWebApp per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="c5619-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c5619-112">PARAMETERS</span></span>

### <span data-ttu-id="c5619-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5619-113">-DefaultProfile</span></span>
<span data-ttu-id="c5619-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c5619-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5619-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="c5619-115">-EndTime</span></span>
<span data-ttu-id="c5619-116">Ora di fine in UTC</span><span class="sxs-lookup"><span data-stu-id="c5619-116">End Time in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5619-117">-Granularità</span><span class="sxs-lookup"><span data-stu-id="c5619-117">-Granularity</span></span>
<span data-ttu-id="c5619-118">Granularità</span><span class="sxs-lookup"><span data-stu-id="c5619-118">Granularity</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PT1M, PT1H, P1D

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5619-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="c5619-119">-InstanceDetails</span></span>
<span data-ttu-id="c5619-120">Dettagli istanza</span><span class="sxs-lookup"><span data-stu-id="c5619-120">Instance Details</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5619-121">-Metriche</span><span class="sxs-lookup"><span data-stu-id="c5619-121">-Metrics</span></span>
<span data-ttu-id="c5619-122">Metriche come matrice di stringhe</span><span class="sxs-lookup"><span data-stu-id="c5619-122">Metrics as a string array</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5619-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="c5619-123">-Name</span></span>
<span data-ttu-id="c5619-124">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="c5619-124">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5619-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5619-125">-ResourceGroupName</span></span>
<span data-ttu-id="c5619-126">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="c5619-126">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5619-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c5619-127">-StartTime</span></span>
<span data-ttu-id="c5619-128">Ora di inizio in UTC</span><span class="sxs-lookup"><span data-stu-id="c5619-128">Start Time in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5619-129">-Web App</span><span class="sxs-lookup"><span data-stu-id="c5619-129">-WebApp</span></span>
<span data-ttu-id="c5619-130">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="c5619-130">WebApp object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5619-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5619-131">CommonParameters</span></span>
<span data-ttu-id="c5619-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5619-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5619-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5619-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5619-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c5619-134">INPUTS</span></span>

### <span data-ttu-id="c5619-135">Sito</span><span class="sxs-lookup"><span data-stu-id="c5619-135">Site</span></span>
<span data-ttu-id="c5619-136">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="c5619-136">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="c5619-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c5619-137">OUTPUTS</span></span>

## <span data-ttu-id="c5619-138">Note</span><span class="sxs-lookup"><span data-stu-id="c5619-138">NOTES</span></span>

## <span data-ttu-id="c5619-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c5619-139">RELATED LINKS</span></span>

[<span data-ttu-id="c5619-140">Get-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="c5619-140">Get-AzWebAppCertificate</span></span>](./Get-AzWebAppCertificate.md)

