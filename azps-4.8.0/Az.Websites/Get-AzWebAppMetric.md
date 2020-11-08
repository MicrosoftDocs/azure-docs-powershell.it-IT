---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 513BE097-EB4A-4C49-9F7F-42A2BED09022
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppMetric.md
ms.openlocfilehash: 91b5de48805e458b771227ca9c92e9891be170e1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192615"
---
# <span data-ttu-id="66e87-101">Get-AzWebAppMetric</span><span class="sxs-lookup"><span data-stu-id="66e87-101">Get-AzWebAppMetric</span></span>

## <span data-ttu-id="66e87-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="66e87-102">SYNOPSIS</span></span>
<span data-ttu-id="66e87-103">Ottiene le metriche di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="66e87-103">Gets Azure Web App metrics.</span></span>

## <span data-ttu-id="66e87-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="66e87-104">SYNTAX</span></span>

### <span data-ttu-id="66e87-105">S1</span><span class="sxs-lookup"><span data-stu-id="66e87-105">S1</span></span>
```
Get-AzWebAppMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66e87-106">S2</span><span class="sxs-lookup"><span data-stu-id="66e87-106">S2</span></span>
```
Get-AzWebAppMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="66e87-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="66e87-107">DESCRIPTION</span></span>
<span data-ttu-id="66e87-108">Il **Get-AzWebAppMetric** ottiene le metriche delle app Web.</span><span class="sxs-lookup"><span data-stu-id="66e87-108">The **Get-AzWebAppMetric** gets Web App metrics.</span></span>

## <span data-ttu-id="66e87-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="66e87-109">EXAMPLES</span></span>

### <span data-ttu-id="66e87-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="66e87-110">Example 1</span></span>
```
PS C:\> Get-AzAppServicePlanMetric -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics "Requests"
```

<span data-ttu-id="66e87-111">Questo comando ottiene le richieste dell'app Web ContosoWebApp al minuto (PT1M-polling Time 1 minute) tra StartTime e EndTime</span><span class="sxs-lookup"><span data-stu-id="66e87-111">This command gets Requests of the Web App ContosoWebApp per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="66e87-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="66e87-112">PARAMETERS</span></span>

### <span data-ttu-id="66e87-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66e87-113">-DefaultProfile</span></span>
<span data-ttu-id="66e87-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="66e87-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66e87-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="66e87-115">-EndTime</span></span>
<span data-ttu-id="66e87-116">Ora di fine in UTC</span><span class="sxs-lookup"><span data-stu-id="66e87-116">End Time in UTC</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66e87-117">-Granularità</span><span class="sxs-lookup"><span data-stu-id="66e87-117">-Granularity</span></span>
<span data-ttu-id="66e87-118">Granularità</span><span class="sxs-lookup"><span data-stu-id="66e87-118">Granularity</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PT1M, PT1H, P1D

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66e87-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="66e87-119">-InstanceDetails</span></span>
<span data-ttu-id="66e87-120">Dettagli istanza</span><span class="sxs-lookup"><span data-stu-id="66e87-120">Instance Details</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66e87-121">-Metriche</span><span class="sxs-lookup"><span data-stu-id="66e87-121">-Metrics</span></span>
<span data-ttu-id="66e87-122">Metriche come matrice di stringhe</span><span class="sxs-lookup"><span data-stu-id="66e87-122">Metrics as a string array</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66e87-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="66e87-123">-Name</span></span>
<span data-ttu-id="66e87-124">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="66e87-124">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66e87-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66e87-125">-ResourceGroupName</span></span>
<span data-ttu-id="66e87-126">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="66e87-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66e87-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="66e87-127">-StartTime</span></span>
<span data-ttu-id="66e87-128">Ora di inizio in UTC</span><span class="sxs-lookup"><span data-stu-id="66e87-128">Start Time in UTC</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66e87-129">-Web App</span><span class="sxs-lookup"><span data-stu-id="66e87-129">-WebApp</span></span>
<span data-ttu-id="66e87-130">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="66e87-130">WebApp object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66e87-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66e87-131">CommonParameters</span></span>
<span data-ttu-id="66e87-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66e87-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66e87-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="66e87-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66e87-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="66e87-134">INPUTS</span></span>

### <span data-ttu-id="66e87-135">System. String</span><span class="sxs-lookup"><span data-stu-id="66e87-135">System.String</span></span>

### <span data-ttu-id="66e87-136">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="66e87-136">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="66e87-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="66e87-137">OUTPUTS</span></span>

### <span data-ttu-id="66e87-138">Microsoft. Azure. Management. website. Models. ResourceMetric</span><span class="sxs-lookup"><span data-stu-id="66e87-138">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="66e87-139">Note</span><span class="sxs-lookup"><span data-stu-id="66e87-139">NOTES</span></span>

## <span data-ttu-id="66e87-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="66e87-140">RELATED LINKS</span></span>

[<span data-ttu-id="66e87-141">Get-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="66e87-141">Get-AzWebAppCertificate</span></span>](./Get-AzWebAppCertificate.md)
