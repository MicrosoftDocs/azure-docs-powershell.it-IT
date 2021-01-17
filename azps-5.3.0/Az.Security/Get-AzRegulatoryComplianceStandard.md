---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzRegulatoryComplianceStandard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceStandard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceStandard.md
ms.openlocfilehash: a554a0adcdf8692f054becb5891cdd0c20203911
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486375"
---
# <span data-ttu-id="80473-101">Get-AzRegulatoryComplianceStandard</span><span class="sxs-lookup"><span data-stu-id="80473-101">Get-AzRegulatoryComplianceStandard</span></span>

## <span data-ttu-id="80473-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="80473-102">SYNOPSIS</span></span>
<span data-ttu-id="80473-103">Ottiene gli standard di conformità regulatoey</span><span class="sxs-lookup"><span data-stu-id="80473-103">Gets regulatoey compliance standards</span></span>

## <span data-ttu-id="80473-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="80473-104">SYNTAX</span></span>

### <span data-ttu-id="80473-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="80473-105">SubscriptionScope (Default)</span></span>
```
Get-AzRegulatoryComplianceStandard [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80473-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="80473-106">SubscriptionLevelResource</span></span>
```
Get-AzRegulatoryComplianceStandard -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="80473-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="80473-107">ResourceId</span></span>
```
Get-AzRegulatoryComplianceStandard -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="80473-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="80473-108">DESCRIPTION</span></span>
<span data-ttu-id="80473-109">Ottenere un spcific normative satandard o elencare tutti gli standard di conformità normativi in un abbonamento specifico.</span><span class="sxs-lookup"><span data-stu-id="80473-109">Get a spcific regulatory compliance satandard details or list all regulatory compliance standards under specific subscription.</span></span>

## <span data-ttu-id="80473-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="80473-110">EXAMPLES</span></span>

### <span data-ttu-id="80473-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="80473-111">Example 1</span></span>
```powershell
PS C:\>Get-AzRegulatoryComplianceStandard

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/Azure-CIS-1.1.0
Name                : Azure-CIS-1.1.0
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 20
FailedControls      : 4
SkippedControls     : 0
UnsupportedControls : 87

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/ISO-27001
Name                : ISO-27001
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 9
FailedControls      : 10
SkippedControls     : 2
UnsupportedControls : 93

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/PCI-DSS-3.2.1
Name                : PCI-DSS-3.2.1
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 13
FailedControls      : 32
SkippedControls     : 0
UnsupportedControls : 187

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/SOC-TSP
Name                : SOC-TSP
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 2
FailedControls      : 11
SkippedControls     : 0
UnsupportedControls : 24
```

<span data-ttu-id="80473-112">Ottenere tutti gli standard di conformità normativi in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="80473-112">Get all regulatory compliance standards under a subscription.</span></span>

### <span data-ttu-id="80473-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="80473-113">Example 2</span></span>
```powershell
PS C:\>Get-AzRegulatoryComplianceStandard -Name "SOC-TSP"

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/SOC-TSP
Name                : SOC-TSP
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 2
FailedControls      : 11
SkippedControls     : 0
UnsupportedControls : 24
```

<span data-ttu-id="80473-114">Ottenere i dettagli di specifici standard di conformità normativi secondo il nome standard.</span><span class="sxs-lookup"><span data-stu-id="80473-114">Get details of specific regulatory compliance standard according standard name.</span></span>

### <span data-ttu-id="80473-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="80473-115">Example 3</span></span>
```powershell
PS C:\>Get-AzRegulatoryComplianceStandard -ResourceId "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplianceStandards/SOC-TSP"

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/SOC-TSP
Name                : SOC-TSP
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 2
FailedControls      : 11
SkippedControls     : 0
UnsupportedControls : 24
```

<span data-ttu-id="80473-116">Ottenere i dettagli di specifici standard di conformità normativi secondo l'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="80473-116">Get details of specific regulatory compliance standard according resource id.</span></span>

## <span data-ttu-id="80473-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="80473-117">PARAMETERS</span></span>

### <span data-ttu-id="80473-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80473-118">-DefaultProfile</span></span>
<span data-ttu-id="80473-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="80473-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80473-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="80473-120">-Name</span></span>
<span data-ttu-id="80473-121">Nome standard.</span><span class="sxs-lookup"><span data-stu-id="80473-121">Standard name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80473-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="80473-122">-ResourceId</span></span>
<span data-ttu-id="80473-123">ID della risorsa di sicurezza a cui si vuole richiamare il comando.</span><span class="sxs-lookup"><span data-stu-id="80473-123">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80473-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80473-124">CommonParameters</span></span>
<span data-ttu-id="80473-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80473-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80473-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80473-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80473-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="80473-127">INPUTS</span></span>

### <span data-ttu-id="80473-128">System. String</span><span class="sxs-lookup"><span data-stu-id="80473-128">System.String</span></span>

## <span data-ttu-id="80473-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="80473-129">OUTPUTS</span></span>

### <span data-ttu-id="80473-130">Microsoft. Azure. Commands. SecurityCenter. Models. RegulatoryCompliance. PSSecurityRegulatoryComplianceStandard</span><span class="sxs-lookup"><span data-stu-id="80473-130">Microsoft.Azure.Commands.SecurityCenter.Models.RegulatoryCompliance.PSSecurityRegulatoryComplianceStandard</span></span>

## <span data-ttu-id="80473-131">Note</span><span class="sxs-lookup"><span data-stu-id="80473-131">NOTES</span></span>

## <span data-ttu-id="80473-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="80473-132">RELATED LINKS</span></span>
