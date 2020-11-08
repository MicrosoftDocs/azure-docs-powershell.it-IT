---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzRegulatoryComplianceControl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceControl.md
ms.openlocfilehash: 11c6c1073f53ba4a4b93fdae02ae6f6eb22e0f04
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190115"
---
# <span data-ttu-id="9672b-101">Get-AzRegulatoryComplianceControl</span><span class="sxs-lookup"><span data-stu-id="9672b-101">Get-AzRegulatoryComplianceControl</span></span>

## <span data-ttu-id="9672b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9672b-102">SYNOPSIS</span></span>
<span data-ttu-id="9672b-103">Ottiene i controlli di conformità normativi</span><span class="sxs-lookup"><span data-stu-id="9672b-103">Gets regulatory compliance controls</span></span>

## <span data-ttu-id="9672b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9672b-104">SYNTAX</span></span>

### <span data-ttu-id="9672b-105">SubscriptionLevelResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9672b-105">SubscriptionLevelResource (Default)</span></span>
```
Get-AzRegulatoryComplianceControl [-Name <String>] -StandardName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9672b-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9672b-106">ResourceId</span></span>
```
Get-AzRegulatoryComplianceControl -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9672b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9672b-107">DESCRIPTION</span></span>
<span data-ttu-id="9672b-108">Ottenere i dettagli del controllo spcific o elencare tutti i controlli in uno specifico standard di conformità normativo.</span><span class="sxs-lookup"><span data-stu-id="9672b-108">Get a spcific control details or list all the controls under specific regulatory compliance standard.</span></span>

## <span data-ttu-id="9672b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9672b-109">EXAMPLES</span></span>

### <span data-ttu-id="9672b-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9672b-110">Example 1</span></span>
```powershell
PS C:\> Get-AzRegulatoryComplianceControl -StandardName "SOC TSP"

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/A1.1
Name               : A1.1
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Current processing capacity and usage are maintained, monitored, and evaluated to manage capacity
                     demand and to enable the implementation of additional capacity to help meet the entity�s
                     availability commitments and system requirements.
State              : Unsupported
PassedAssessments  : 0
FailedAssessments  : 0
SkippedAssessments : 0

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/A1.2
Name               : A1.2
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Environmental protections, software, data backup processes, and recovery infrastructure are
                     designed, developed, implemented, operated, maintained, and monitored to meet availability
                     commitments and requirements.
State              : Passed
PassedAssessments  : 3
FailedAssessments  : 0
SkippedAssessments : 0

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/A1.3
Name               : A1.3
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Recovery plan procedures supporting system recovery are tested to help meet the entity�s
                     availability commitments and system requirements.
State              : Unsupported
PassedAssessments  : 0
FailedAssessments  : 0
SkippedAssessments : 0

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/C1.1
Name               : C1.1
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Confidential information is protected during the system design, development, testing,
                     implementation, and change processes in accordance with confidentiality commitments and
                     requirements.
State              : Unsupported
PassedAssessments  : 0
FailedAssessments  : 0
SkippedAssessments : 0
```

<span data-ttu-id="9672b-111">Ottenere tutti i controlli in standard normativi specifici.</span><span class="sxs-lookup"><span data-stu-id="9672b-111">Get all controls under specific regulatory standard.</span></span>

### <span data-ttu-id="9672b-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9672b-112">Example 2</span></span>
```powershell
PS C:\> Get-AzRegulatoryComplianceControl -StandardName "SOC TSP" -Name "C1.2"

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/C1.2
Name               : C1.2
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Confidential information within the boundaries of the system is protected against unauthorized
                     access, use, and disclosure during input, processing, retention, output, and disposition in
                     accordance with confidentiality commitments and requirements.
State              : Failed
PassedAssessments  : 177
FailedAssessments  : 22
SkippedAssessments : 0
```

<span data-ttu-id="9672b-113">Ottenere dettagli di controllo specifici in base all'ID controllo.</span><span class="sxs-lookup"><span data-stu-id="9672b-113">Get specific control details according to control id.</span></span>

### <span data-ttu-id="9672b-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="9672b-114">Example 3</span></span>
```powershell
PS C:\> Get-AzRegulatoryComplianceControl -ResourceId "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/C1.2"

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/C1.2
Name               : C1.2
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Confidential information within the boundaries of the system is protected against unauthorized
                     access, use, and disclosure during input, processing, retention, output, and disposition in
                     accordance with confidentiality commitments and requirements.
State              : Failed
PassedAssessments  : 177
FailedAssessments  : 22
SkippedAssessments : 0
```

<span data-ttu-id="9672b-115">Ottenere dettagli del controllo specifici in base all'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="9672b-115">Get specific control details according to resource id.</span></span>

## <span data-ttu-id="9672b-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9672b-116">PARAMETERS</span></span>

### <span data-ttu-id="9672b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9672b-117">-DefaultProfile</span></span>
<span data-ttu-id="9672b-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9672b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9672b-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="9672b-119">-Name</span></span>
<span data-ttu-id="9672b-120">ID controllo.</span><span class="sxs-lookup"><span data-stu-id="9672b-120">Control Id.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9672b-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9672b-121">-ResourceId</span></span>
<span data-ttu-id="9672b-122">ID della risorsa di sicurezza a cui si vuole richiamare il comando.</span><span class="sxs-lookup"><span data-stu-id="9672b-122">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="9672b-123">-StandardName</span><span class="sxs-lookup"><span data-stu-id="9672b-123">-StandardName</span></span>
<span data-ttu-id="9672b-124">Nome standard.</span><span class="sxs-lookup"><span data-stu-id="9672b-124">Standard Name.</span></span>

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

### <span data-ttu-id="9672b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9672b-125">CommonParameters</span></span>
<span data-ttu-id="9672b-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9672b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9672b-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9672b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9672b-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9672b-128">INPUTS</span></span>

### <span data-ttu-id="9672b-129">System. String</span><span class="sxs-lookup"><span data-stu-id="9672b-129">System.String</span></span>

## <span data-ttu-id="9672b-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9672b-130">OUTPUTS</span></span>

### <span data-ttu-id="9672b-131">Microsoft. Azure. Commands. SecurityCenter. Models. RegulatoryCompliance. PSSecurityRegulatoryComplianceControl</span><span class="sxs-lookup"><span data-stu-id="9672b-131">Microsoft.Azure.Commands.SecurityCenter.Models.RegulatoryCompliance.PSSecurityRegulatoryComplianceControl</span></span>

## <span data-ttu-id="9672b-132">Note</span><span class="sxs-lookup"><span data-stu-id="9672b-132">NOTES</span></span>

## <span data-ttu-id="9672b-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9672b-133">RELATED LINKS</span></span>
