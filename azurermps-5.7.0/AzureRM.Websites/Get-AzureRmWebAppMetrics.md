---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 513BE097-EB4A-4C49-9F7F-42A2BED09022
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppMetrics.md
ms.openlocfilehash: c33038289483c2cd48ac63eb09a4a38627c406da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509528"
---
# <span data-ttu-id="d72ca-101">Get-AzureRmWebAppMetrics</span><span class="sxs-lookup"><span data-stu-id="d72ca-101">Get-AzureRmWebAppMetrics</span></span>

## <span data-ttu-id="d72ca-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d72ca-102">SYNOPSIS</span></span>
<span data-ttu-id="d72ca-103">Ottiene le metriche di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="d72ca-103">Gets Azure Web App metrics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d72ca-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d72ca-104">SYNTAX</span></span>

### <span data-ttu-id="d72ca-105">S1</span><span class="sxs-lookup"><span data-stu-id="d72ca-105">S1</span></span>
```
Get-AzureRmWebAppMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d72ca-106">S2</span><span class="sxs-lookup"><span data-stu-id="d72ca-106">S2</span></span>
```
Get-AzureRmWebAppMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d72ca-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d72ca-107">DESCRIPTION</span></span>
<span data-ttu-id="d72ca-108">Il **Get-AzureRmWebAppMetrics** ottiene le metriche delle app Web.</span><span class="sxs-lookup"><span data-stu-id="d72ca-108">The **Get-AzureRmWebAppMetrics** gets Web App metrics.</span></span>

## <span data-ttu-id="d72ca-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d72ca-109">EXAMPLES</span></span>

### <span data-ttu-id="d72ca-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d72ca-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="d72ca-111">Questo comando ottiene le richieste dell'app Web ContosoWebApp al minuto (PT1M-polling Time 1 minute) tra StartTime e EndTime</span><span class="sxs-lookup"><span data-stu-id="d72ca-111">This command gets Requests of the Web App ContosoWebApp per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="d72ca-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d72ca-112">PARAMETERS</span></span>

### <span data-ttu-id="d72ca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d72ca-113">-DefaultProfile</span></span>
<span data-ttu-id="d72ca-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d72ca-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d72ca-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="d72ca-115">-EndTime</span></span>
<span data-ttu-id="d72ca-116">Ora di fine in UTC</span><span class="sxs-lookup"><span data-stu-id="d72ca-116">End Time in UTC</span></span>

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

### <span data-ttu-id="d72ca-117">-Granularità</span><span class="sxs-lookup"><span data-stu-id="d72ca-117">-Granularity</span></span>
<span data-ttu-id="d72ca-118">Granularità</span><span class="sxs-lookup"><span data-stu-id="d72ca-118">Granularity</span></span>

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

### <span data-ttu-id="d72ca-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="d72ca-119">-InstanceDetails</span></span>
<span data-ttu-id="d72ca-120">Dettagli istanza</span><span class="sxs-lookup"><span data-stu-id="d72ca-120">Instance Details</span></span>

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

### <span data-ttu-id="d72ca-121">-Metriche</span><span class="sxs-lookup"><span data-stu-id="d72ca-121">-Metrics</span></span>
<span data-ttu-id="d72ca-122">Metriche come matrice di stringhe</span><span class="sxs-lookup"><span data-stu-id="d72ca-122">Metrics as a string array</span></span>

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

### <span data-ttu-id="d72ca-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="d72ca-123">-Name</span></span>
<span data-ttu-id="d72ca-124">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="d72ca-124">WebApp Name</span></span>

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

### <span data-ttu-id="d72ca-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d72ca-125">-ResourceGroupName</span></span>
<span data-ttu-id="d72ca-126">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="d72ca-126">Resource Group Name</span></span>

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

### <span data-ttu-id="d72ca-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="d72ca-127">-StartTime</span></span>
<span data-ttu-id="d72ca-128">Ora di inizio in UTC</span><span class="sxs-lookup"><span data-stu-id="d72ca-128">Start Time in UTC</span></span>

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

### <span data-ttu-id="d72ca-129">-Web App</span><span class="sxs-lookup"><span data-stu-id="d72ca-129">-WebApp</span></span>
<span data-ttu-id="d72ca-130">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="d72ca-130">WebApp object</span></span>

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

### <span data-ttu-id="d72ca-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d72ca-131">CommonParameters</span></span>
<span data-ttu-id="d72ca-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d72ca-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d72ca-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d72ca-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d72ca-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d72ca-134">INPUTS</span></span>

### <span data-ttu-id="d72ca-135">Sito</span><span class="sxs-lookup"><span data-stu-id="d72ca-135">Site</span></span>
<span data-ttu-id="d72ca-136">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="d72ca-136">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="d72ca-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d72ca-137">OUTPUTS</span></span>

## <span data-ttu-id="d72ca-138">Note</span><span class="sxs-lookup"><span data-stu-id="d72ca-138">NOTES</span></span>

## <span data-ttu-id="d72ca-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d72ca-139">RELATED LINKS</span></span>

[<span data-ttu-id="d72ca-140">Get-AzureRmWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="d72ca-140">Get-AzureRmWebAppCertificate</span></span>](./Get-AzureRmWebAppCertificate.md)

