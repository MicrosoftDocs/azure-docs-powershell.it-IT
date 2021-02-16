---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-AzVMGuestPolicyStatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
ms.openlocfilehash: 49148f1c62b71436e48b2b92a4591a7cdb36cccf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187662"
---
# <span data-ttu-id="56f60-101">Get-AzVMGuestPolicyStatus</span><span class="sxs-lookup"><span data-stu-id="56f60-101">Get-AzVMGuestPolicyStatus</span></span>

## <span data-ttu-id="56f60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56f60-102">SYNOPSIS</span></span>
<span data-ttu-id="56f60-103">Recupera gli stati dei criteri di configurazione guest (dettagliati) per un'iniziativa di tipo "Configurazione guest" assegnata a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="56f60-103">Gets guest configuration policy statuses (detailed) for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="56f60-104">Un'iniziativa è una politica di definizione di tipo "Iniziativa".</span><span class="sxs-lookup"><span data-stu-id="56f60-104">An initiative is a policy of definition type "Initiative".</span></span>

## <span data-ttu-id="56f60-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="56f60-105">SYNTAX</span></span>

### <span data-ttu-id="56f60-106">VmScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="56f60-106">VmScope (Default)</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56f60-107">InitiativeIdScope</span><span class="sxs-lookup"><span data-stu-id="56f60-107">InitiativeIdScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56f60-108">InitiativeNameScope</span><span class="sxs-lookup"><span data-stu-id="56f60-108">InitiativeNameScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56f60-109">ReportIdScope</span><span class="sxs-lookup"><span data-stu-id="56f60-109">ReportIdScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ReportId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56f60-110">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="56f60-110">DESCRIPTION</span></span>
<span data-ttu-id="56f60-111">Il cmdlet Get-AzVMGuestPolicyStatus ottiene gli stati dei criteri di configurazione guest per un'iniziativa di tipo "Configurazione guest" assegnata a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="56f60-111">The Get-AzVMGuestPolicyStatus cmdlet gets guest configuration policy statuses for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="56f60-112">Un'iniziativa è una politica di definizione di tipo "Iniziativa".</span><span class="sxs-lookup"><span data-stu-id="56f60-112">An initiative is a policy of definition type "Initiative".</span></span>
<span data-ttu-id="56f60-113">Questo cmdlet ottiene gli stati di conformità della macchina virtuale e i motivi per cui non è conforme ai singoli criteri nell'iniziativa.</span><span class="sxs-lookup"><span data-stu-id="56f60-113">This cmdlet gets compliance statuses of the VM and reasons why it is non-compliant for the individual policies in the initiative.</span></span>

## <span data-ttu-id="56f60-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="56f60-114">EXAMPLES</span></span>

### <span data-ttu-id="56f60-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="56f60-115">Example 1</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```

<span data-ttu-id="56f60-116">Ottenere tutti gli stati più recenti dei criteri di configurazione guest per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="56f60-116">Get all latest guest configuration policy statuses for a VM.</span></span>
<span data-ttu-id="56f60-117">Lo stato include lo stato di conformità della macchina virtuale per ogni criterio in tutte le iniziative di tipo "Configurazione guest", motivi di conformità, tempo del controllo di conformità, informazioni sulle risorse verificate per conformità.</span><span class="sxs-lookup"><span data-stu-id="56f60-117">The status includes compliance status of the VM for each policy in all initiatives of type "Guest Configuration", compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="56f60-118">I risultati includono gli stati più recenti, non includono gli stati cronologici precedenti.</span><span class="sxs-lookup"><span data-stu-id="56f60-118">The results include latest statuses, does not include previous historical statuses.</span></span>

### <span data-ttu-id="56f60-119">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="56f60-119">Example 2</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

<span data-ttu-id="56f60-120">Ottenere gli stati più recenti dei criteri di configurazione guest in base all'ID iniziativa. Lo stato include lo stato di conformità della macchina virtuale per ogni criterio nell'iniziativa, motivi di conformità, tempo del controllo di conformità, informazioni sulle risorse verificate per conformità.</span><span class="sxs-lookup"><span data-stu-id="56f60-120">Get the latest guest configuration policy statuses by initiative Id. The status includes compliance status of the VM for each policy in the initiative, compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="56f60-121">I risultati non includono gli stati generati in precedenza, ma solo lo stato più recente per ogni criterio dell'iniziativa.</span><span class="sxs-lookup"><span data-stu-id="56f60-121">The results does not include previous statuses generated, it just includes latest status for each policy in the initiative.</span></span>

### <span data-ttu-id="56f60-122">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="56f60-122">Example 3</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

<span data-ttu-id="56f60-123">Ottenere gli stati più recenti dei criteri di configurazione guest in base al nome dell'iniziativa.</span><span class="sxs-lookup"><span data-stu-id="56f60-123">Get the latest guest configuration policy statuses by initiative name.</span></span>
<span data-ttu-id="56f60-124">Lo stato include lo stato di conformità della macchina virtuale per ogni criterio nell'iniziativa, motivi di conformità, tempo del controllo di conformità, informazioni sulle risorse verificate per conformità.</span><span class="sxs-lookup"><span data-stu-id="56f60-124">The status includes compliance status of the VM for each policy in the initiative, compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="56f60-125">I risultati non includono gli stati generati in precedenza, ma solo lo stato più recente per ogni criterio dell'iniziativa.</span><span class="sxs-lookup"><span data-stu-id="56f60-125">The results does not include previous statuses generated, it just includes latest status for each policy in the initiative.</span></span>

### <span data-ttu-id="56f60-126">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="56f60-126">Example 4</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ReportId "/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac"
```

<span data-ttu-id="56f60-127">Ottenere lo stato dei criteri di configurazione guest in base a ReportId.</span><span class="sxs-lookup"><span data-stu-id="56f60-127">Get guest configuration policy status by ReportId.</span></span>
<span data-ttu-id="56f60-128">ReportId è la proprietà ReportId che è possibile trovare nei risultati dell'Get-AzVMGuestPolicyStatus per initiativeId o Initiative Name (vedere altri esempi)</span><span class="sxs-lookup"><span data-stu-id="56f60-128">The ReportId is the ReportId property that can be found in the results of Get-AzVMGuestPolicyStatus by initiativeId or Initiative name (please refer other examples)</span></span>

## <span data-ttu-id="56f60-129">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56f60-129">PARAMETERS</span></span>

### <span data-ttu-id="56f60-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56f60-130">-DefaultProfile</span></span>
<span data-ttu-id="56f60-131">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="56f60-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56f60-132">-InitiativeId</span><span class="sxs-lookup"><span data-stu-id="56f60-132">-InitiativeId</span></span>
<span data-ttu-id="56f60-133">ID definizione di un criterio in cui il tipo di definizione è Initiative e la categoria è Guest Configuration</span><span class="sxs-lookup"><span data-stu-id="56f60-133">Definition Id of a policy where definition type is Initiative and category is Guest Configuration</span></span>

```yaml
Type: System.String
Parameter Sets: InitiativeIdScope
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56f60-134">-InitiativeName</span><span class="sxs-lookup"><span data-stu-id="56f60-134">-InitiativeName</span></span>
<span data-ttu-id="56f60-135">Nome di un criterio in cui il tipo di definizione è Iniziativa e la categoria è Configurazione guest</span><span class="sxs-lookup"><span data-stu-id="56f60-135">Name of a policy where definition type is Initiative and category is Guest Configuration</span></span>

```yaml
Type: System.String
Parameter Sets: InitiativeNameScope
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56f60-136">-ReportId</span><span class="sxs-lookup"><span data-stu-id="56f60-136">-ReportId</span></span>
<span data-ttu-id="56f60-137">ID dello stato dei criteri di configurazione guest.</span><span class="sxs-lookup"><span data-stu-id="56f60-137">Id of a Guest Configuration policy status.</span></span>
<span data-ttu-id="56f60-138">Un criterio in cui il tipo di definizione è Iniziativa e la categoria è Configurazione guest deve essere assegnato a un ambito per ottenere gli stati.</span><span class="sxs-lookup"><span data-stu-id="56f60-138">A policy where definition type is Initiative and category is Guest Configuration must be assigned to a scope to get statuses.</span></span>

```yaml
Type: System.String
Parameter Sets: ReportIdScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56f60-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56f60-139">-ResourceGroupName</span></span>
<span data-ttu-id="56f60-140">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="56f60-140">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: VmScope, InitiativeIdScope, InitiativeNameScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56f60-141">-VMName</span><span class="sxs-lookup"><span data-stu-id="56f60-141">-VMName</span></span>
<span data-ttu-id="56f60-142">Nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="56f60-142">VM name.</span></span>

```yaml
Type: System.String
Parameter Sets: VmScope, InitiativeIdScope, InitiativeNameScope
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56f60-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56f60-143">CommonParameters</span></span>
<span data-ttu-id="56f60-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56f60-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56f60-145">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56f60-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56f60-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="56f60-146">INPUTS</span></span>

### <span data-ttu-id="56f60-147">Nessuno</span><span class="sxs-lookup"><span data-stu-id="56f60-147">None</span></span>
## <span data-ttu-id="56f60-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="56f60-148">OUTPUTS</span></span>

### <span data-ttu-id="56f60-149">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatusDetailed</span><span class="sxs-lookup"><span data-stu-id="56f60-149">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatusDetailed</span></span>
## <span data-ttu-id="56f60-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="56f60-150">NOTES</span></span>

## <span data-ttu-id="56f60-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="56f60-151">RELATED LINKS</span></span>
