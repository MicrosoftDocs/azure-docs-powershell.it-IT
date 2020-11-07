---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-AzVMGuestPolicyStatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
ms.openlocfilehash: c1bf608c76c547360d9d7a48f4ba74c1713ee049
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836100"
---
# <span data-ttu-id="b600b-101">Get-AzVMGuestPolicyStatus</span><span class="sxs-lookup"><span data-stu-id="b600b-101">Get-AzVMGuestPolicyStatus</span></span>

## <span data-ttu-id="b600b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b600b-102">SYNOPSIS</span></span>
<span data-ttu-id="b600b-103">Ottiene gli Stati dei criteri di configurazione Guest (dettagliati) per un'iniziativa di tipo "configurazione Guest" assegnata a una VM.</span><span class="sxs-lookup"><span data-stu-id="b600b-103">Gets guest configuration policy statuses (detailed) for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="b600b-104">Un'iniziativa è un criterio di tipo definizione "iniziativa".</span><span class="sxs-lookup"><span data-stu-id="b600b-104">An initiative is a policy of definition type "Initiative".</span></span>

## <span data-ttu-id="b600b-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b600b-105">SYNTAX</span></span>

### <span data-ttu-id="b600b-106">VmScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b600b-106">VmScope (Default)</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b600b-107">InitiativeIdScope</span><span class="sxs-lookup"><span data-stu-id="b600b-107">InitiativeIdScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b600b-108">InitiativeNameScope</span><span class="sxs-lookup"><span data-stu-id="b600b-108">InitiativeNameScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b600b-109">ReportIdScope</span><span class="sxs-lookup"><span data-stu-id="b600b-109">ReportIdScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ReportId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b600b-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b600b-110">DESCRIPTION</span></span>
<span data-ttu-id="b600b-111">Il cmdlet Get-AzVMGuestPolicyStatus ottiene gli Stati dei criteri di configurazione Guest per un'iniziativa di tipo "configurazione Guest" assegnata a una VM.</span><span class="sxs-lookup"><span data-stu-id="b600b-111">The Get-AzVMGuestPolicyStatus cmdlet gets guest configuration policy statuses for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="b600b-112">Un'iniziativa è un criterio di tipo definizione "iniziativa".</span><span class="sxs-lookup"><span data-stu-id="b600b-112">An initiative is a policy of definition type "Initiative".</span></span>
<span data-ttu-id="b600b-113">Questo cmdlet ottiene gli Stati di conformità della VM e i motivi per cui non è conforme ai singoli criteri dell'iniziativa.</span><span class="sxs-lookup"><span data-stu-id="b600b-113">This cmdlet gets compliance statuses of the VM and reasons why it is non-compliant for the individual policies in the initiative.</span></span>

## <span data-ttu-id="b600b-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b600b-114">EXAMPLES</span></span>

### <span data-ttu-id="b600b-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b600b-115">Example 1</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```

<span data-ttu-id="b600b-116">Ottenere tutti gli ultimi stati dei criteri di configurazione Guest per una VM.</span><span class="sxs-lookup"><span data-stu-id="b600b-116">Get all latest guest configuration policy statuses for a VM.</span></span>
<span data-ttu-id="b600b-117">Lo stato include lo stato di conformità della VM per ogni criterio in tutte le iniziative di tipo "configurazione Guest", motivi di conformità, ora del controllo di conformità, informazioni sulle risorse controllate per la conformità.</span><span class="sxs-lookup"><span data-stu-id="b600b-117">The status includes compliance status of the VM for each policy in all initiatives of type "Guest Configuration", compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="b600b-118">I risultati includono gli ultimi Stati, non includono gli Stati storici precedenti.</span><span class="sxs-lookup"><span data-stu-id="b600b-118">The results include latest statuses, does not include previous historical statuses.</span></span>

### <span data-ttu-id="b600b-119">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b600b-119">Example 2</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

<span data-ttu-id="b600b-120">Ottenere gli ultimi stati dei criteri di configurazione Guest per ID iniziativa. Lo stato include lo stato di conformità della VM per ogni criterio nell'iniziativa, i motivi di conformità, l'ora del controllo di conformità, le informazioni sulle risorse controllate per la conformità.</span><span class="sxs-lookup"><span data-stu-id="b600b-120">Get the latest guest configuration policy statuses by initiative Id. The status includes compliance status of the VM for each policy in the initiative, compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="b600b-121">I risultati non includono gli stati precedenti generati, ma include solo lo stato più recente per ogni criterio nell'iniziativa.</span><span class="sxs-lookup"><span data-stu-id="b600b-121">The results does not include previous statuses generated, it just includes latest status for each policy in the initiative.</span></span>

### <span data-ttu-id="b600b-122">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="b600b-122">Example 3</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

<span data-ttu-id="b600b-123">Ottenere gli ultimi stati dei criteri di configurazione Guest per nome iniziativa.</span><span class="sxs-lookup"><span data-stu-id="b600b-123">Get the latest guest configuration policy statuses by initiative name.</span></span>
<span data-ttu-id="b600b-124">Lo stato include lo stato di conformità della VM per ogni criterio nell'iniziativa, i motivi di conformità, l'ora del controllo di conformità, le informazioni sulle risorse controllate per la conformità.</span><span class="sxs-lookup"><span data-stu-id="b600b-124">The status includes compliance status of the VM for each policy in the initiative, compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="b600b-125">I risultati non includono gli stati precedenti generati, ma include solo lo stato più recente per ogni criterio nell'iniziativa.</span><span class="sxs-lookup"><span data-stu-id="b600b-125">The results does not include previous statuses generated, it just includes latest status for each policy in the initiative.</span></span>

### <span data-ttu-id="b600b-126">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="b600b-126">Example 4</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ReportId "/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac"
```

<span data-ttu-id="b600b-127">Ottenere lo stato dei criteri di configurazione Guest in ReportId.</span><span class="sxs-lookup"><span data-stu-id="b600b-127">Get guest configuration policy status by ReportId.</span></span>
<span data-ttu-id="b600b-128">ReportId è la proprietà ReportId che si trova nei risultati di Get-AzVMGuestPolicyStatus in base a initiativeId o nome dell'iniziativa (vedere altri esempi)</span><span class="sxs-lookup"><span data-stu-id="b600b-128">The ReportId is the ReportId property that can be found in the results of Get-AzVMGuestPolicyStatus by initiativeId or Initiative name (please refer other examples)</span></span>

## <span data-ttu-id="b600b-129">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b600b-129">PARAMETERS</span></span>

### <span data-ttu-id="b600b-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b600b-130">-DefaultProfile</span></span>
<span data-ttu-id="b600b-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b600b-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b600b-132">-InitiativeId</span><span class="sxs-lookup"><span data-stu-id="b600b-132">-InitiativeId</span></span>
<span data-ttu-id="b600b-133">ID definizione di un criterio in cui il tipo di definizione è Initiative e Category è la configurazione Guest</span><span class="sxs-lookup"><span data-stu-id="b600b-133">Definition Id of a policy where definition type is Initiative and category is Guest Configuration</span></span>

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

### <span data-ttu-id="b600b-134">-Initiativename</span><span class="sxs-lookup"><span data-stu-id="b600b-134">-InitiativeName</span></span>
<span data-ttu-id="b600b-135">Nome di un criterio in cui il tipo di definizione è Initiative e Category è la configurazione Guest</span><span class="sxs-lookup"><span data-stu-id="b600b-135">Name of a policy where definition type is Initiative and category is Guest Configuration</span></span>

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

### <span data-ttu-id="b600b-136">-ReportId</span><span class="sxs-lookup"><span data-stu-id="b600b-136">-ReportId</span></span>
<span data-ttu-id="b600b-137">ID di uno stato dei criteri di configurazione Guest.</span><span class="sxs-lookup"><span data-stu-id="b600b-137">Id of a Guest Configuration policy status.</span></span>
<span data-ttu-id="b600b-138">Un criterio in cui il tipo di definizione è iniziativa e la categoria è la configurazione Guest deve essere assegnata a un ambito per ottenere gli Stati.</span><span class="sxs-lookup"><span data-stu-id="b600b-138">A policy where definition type is Initiative and category is Guest Configuration must be assigned to a scope to get statuses.</span></span>

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

### <span data-ttu-id="b600b-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b600b-139">-ResourceGroupName</span></span>
<span data-ttu-id="b600b-140">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b600b-140">Resource group name.</span></span>

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

### <span data-ttu-id="b600b-141">-VMName</span><span class="sxs-lookup"><span data-stu-id="b600b-141">-VMName</span></span>
<span data-ttu-id="b600b-142">Nome VM.</span><span class="sxs-lookup"><span data-stu-id="b600b-142">VM name.</span></span>

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

### <span data-ttu-id="b600b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b600b-143">CommonParameters</span></span>
<span data-ttu-id="b600b-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b600b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b600b-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b600b-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b600b-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b600b-146">INPUTS</span></span>

### <span data-ttu-id="b600b-147">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b600b-147">None</span></span>
## <span data-ttu-id="b600b-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b600b-148">OUTPUTS</span></span>

### <span data-ttu-id="b600b-149">Microsoft. Azure. Commands. GuestConfiguration. Models. PolicyStatusDetailed</span><span class="sxs-lookup"><span data-stu-id="b600b-149">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatusDetailed</span></span>
## <span data-ttu-id="b600b-150">Note</span><span class="sxs-lookup"><span data-stu-id="b600b-150">NOTES</span></span>

## <span data-ttu-id="b600b-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b600b-151">RELATED LINKS</span></span>
