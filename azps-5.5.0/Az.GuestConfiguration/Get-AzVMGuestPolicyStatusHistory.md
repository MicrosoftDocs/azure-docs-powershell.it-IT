---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-azvmguestpolicystatushistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
ms.openlocfilehash: 929bc417cf4b84800635b85e7f503972509aa7fc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204035"
---
# <span data-ttu-id="86d9b-101">Get-AzVMGuestPolicyStatusHistory</span><span class="sxs-lookup"><span data-stu-id="86d9b-101">Get-AzVMGuestPolicyStatusHistory</span></span>

## <span data-ttu-id="86d9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86d9b-102">SYNOPSIS</span></span>
<span data-ttu-id="86d9b-103">Recupera la cronologia dello stato di conformità dei criteri di configurazione guest per un'iniziativa di tipo "Configurazione guest" assegnata a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="86d9b-103">Gets guest configuration policy compliance status history for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="86d9b-104">Un'iniziativa è una politica di definizione di tipo "Iniziativa".</span><span class="sxs-lookup"><span data-stu-id="86d9b-104">An initiative is a policy of definition type "Initiative".</span></span>

## <span data-ttu-id="86d9b-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="86d9b-105">SYNTAX</span></span>

### <span data-ttu-id="86d9b-106">InitiativeNameScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="86d9b-106">InitiativeNameScope (Default)</span></span>
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86d9b-107">InitiativeIdScope</span><span class="sxs-lookup"><span data-stu-id="86d9b-107">InitiativeIdScope</span></span>
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [[-InitiativeId] <String>]
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86d9b-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="86d9b-108">DESCRIPTION</span></span>
<span data-ttu-id="86d9b-109">Il Get-AzVMGuestPolicyStatusHistory cmdlet ottiene la cronologia dello stato di conformità dei criteri di configurazione guest per un'iniziativa di tipo "Configurazione guest" assegnata a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="86d9b-109">The Get-AzVMGuestPolicyStatusHistory cmdlet gets compliance status history of guest configuration policies for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="86d9b-110">Un'iniziativa è una politica di definizione di tipo "Iniziativa".</span><span class="sxs-lookup"><span data-stu-id="86d9b-110">An initiative is a policy of definition type "Initiative".</span></span>
<span data-ttu-id="86d9b-111">Usare Get-AzVMGuestPolicyStatus cmdlet per ottenere dettagli su un singolo stato di conformità usando ReportId, disponibile nell'output del cmdlet Get-AzVMGuestPolicyStatusHistory.</span><span class="sxs-lookup"><span data-stu-id="86d9b-111">Use Get-AzVMGuestPolicyStatus cmdlet to get details of a single compliance status using ReportId that can be found in output of Get-AzVMGuestPolicyStatusHistory cmdlet.</span></span>

## <span data-ttu-id="86d9b-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="86d9b-112">EXAMPLES</span></span>

### <span data-ttu-id="86d9b-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="86d9b-113">Example 1</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af" -ShowOnlyChange
```

<span data-ttu-id="86d9b-114">Recupera la cronologia dello stato di conformità in base all'ID dell'iniziativa. L'opzione ShowOnlyChange mostra solo le modifiche cronologiche apportate allo stato.</span><span class="sxs-lookup"><span data-stu-id="86d9b-114">Gets compliance status history by initiative Id. ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="86d9b-115">Ignora gli stati che non sono stati modificati tra due controlli di conformità.</span><span class="sxs-lookup"><span data-stu-id="86d9b-115">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="86d9b-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="86d9b-116">Example 2</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17" -ShowOnlyChange
```

<span data-ttu-id="86d9b-117">Recupera la cronologia dello stato di conformità in base al nome dell'iniziativa.</span><span class="sxs-lookup"><span data-stu-id="86d9b-117">Gets compliance status history by initiative name.</span></span>
<span data-ttu-id="86d9b-118">L'opzione ShowOnlyChange mostra solo le modifiche cronologiche apportate allo stato.</span><span class="sxs-lookup"><span data-stu-id="86d9b-118">ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="86d9b-119">Ignora gli stati che non sono stati modificati tra due controlli di conformità.</span><span class="sxs-lookup"><span data-stu-id="86d9b-119">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="86d9b-120">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="86d9b-120">Example 3</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -ShowOnlyChange
```

<span data-ttu-id="86d9b-121">Recupera la cronologia dello stato di conformità per tutti i criteri di configurazione guest assegnati alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="86d9b-121">Gets compliance status history for all guest configuration policies assigned to the VM.</span></span>
<span data-ttu-id="86d9b-122">L'opzione ShowOnlyChange mostra solo le modifiche cronologiche apportate allo stato.</span><span class="sxs-lookup"><span data-stu-id="86d9b-122">ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="86d9b-123">Ignora gli stati che non sono stati modificati tra due controlli di conformità.</span><span class="sxs-lookup"><span data-stu-id="86d9b-123">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="86d9b-124">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="86d9b-124">Example 4</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

<span data-ttu-id="86d9b-125">Recupera la cronologia dello stato di conformità in base all'ID iniziativa.</span><span class="sxs-lookup"><span data-stu-id="86d9b-125">Gets compliance status history by initiative Id.</span></span>

### <span data-ttu-id="86d9b-126">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="86d9b-126">Example 5</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

<span data-ttu-id="86d9b-127">Recupera la cronologia dello stato di conformità in base al nome dell'iniziativa.</span><span class="sxs-lookup"><span data-stu-id="86d9b-127">Gets compliance status history by initiative name.</span></span>

### <span data-ttu-id="86d9b-128">Esempio 6</span><span class="sxs-lookup"><span data-stu-id="86d9b-128">Example 6</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```
<span data-ttu-id="86d9b-129">Recupera la cronologia dello stato di conformità per tutti i criteri di configurazione guest assegnati alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="86d9b-129">Gets compliance status history for all guest configuration policies assigned to the VM.</span></span>

### <span data-ttu-id="86d9b-130">Esempio 7</span><span class="sxs-lookup"><span data-stu-id="86d9b-130">Example 7</span></span>
```powershell
PS C:\>$x = Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
PS C:\>$x[10].ReportId
/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac
PS C:\> Get-AzVMGuestPolicyStatus -ReportId $x[10].ReportId
```

<span data-ttu-id="86d9b-131">Ottenere lo stato dei criteri di configurazione guest in base a ReportId.</span><span class="sxs-lookup"><span data-stu-id="86d9b-131">Get guest configuration policy status by ReportId.</span></span>
<span data-ttu-id="86d9b-132">ReportId è la proprietà ReportId che è possibile trovare nei risultati di Get-AzVMGuestPolicyStatusHistory.</span><span class="sxs-lookup"><span data-stu-id="86d9b-132">The ReportId is the ReportId property that can be found in the results of Get-AzVMGuestPolicyStatusHistory.</span></span> <span data-ttu-id="86d9b-133">(fai riferimento ad altri esempi)</span><span class="sxs-lookup"><span data-stu-id="86d9b-133">(please refer other examples)</span></span>

## <span data-ttu-id="86d9b-134">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86d9b-134">PARAMETERS</span></span>

### <span data-ttu-id="86d9b-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86d9b-135">-DefaultProfile</span></span>
<span data-ttu-id="86d9b-136">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="86d9b-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86d9b-137">-InitiativeId</span><span class="sxs-lookup"><span data-stu-id="86d9b-137">-InitiativeId</span></span>
<span data-ttu-id="86d9b-138">ID definizione di un criterio in cui il tipo di definizione è Initiative e la categoria è Guest Configuration</span><span class="sxs-lookup"><span data-stu-id="86d9b-138">Definition Id of a policy where definition type is Initiative and category is Guest Configuration</span></span>

```yaml
Type: System.String
Parameter Sets: InitiativeIdScope
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86d9b-139">-InitiativeName</span><span class="sxs-lookup"><span data-stu-id="86d9b-139">-InitiativeName</span></span>
<span data-ttu-id="86d9b-140">Nome di un criterio in cui il tipo di definizione è Iniziativa e la categoria è Configurazione guest</span><span class="sxs-lookup"><span data-stu-id="86d9b-140">Name of a policy where definition type is Initiative and category is Guest Configuration</span></span>

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

### <span data-ttu-id="86d9b-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86d9b-141">-ResourceGroupName</span></span>
<span data-ttu-id="86d9b-142">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="86d9b-142">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86d9b-143">-ShowOnlyChange</span><span class="sxs-lookup"><span data-stu-id="86d9b-143">-ShowOnlyChange</span></span>
<span data-ttu-id="86d9b-144">Mostra le modifiche dello stato cronologiche solo per i criteri di configurazione guest.</span><span class="sxs-lookup"><span data-stu-id="86d9b-144">Shows historical status changes only for guest configuration policies.</span></span>
<span data-ttu-id="86d9b-145">Ignora gli stati che non sono stati modificati tra due controlli dello stato di conformità.</span><span class="sxs-lookup"><span data-stu-id="86d9b-145">Skips statuses that have not changed between two compliance status audit runs.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86d9b-146">-VMName</span><span class="sxs-lookup"><span data-stu-id="86d9b-146">-VMName</span></span>
<span data-ttu-id="86d9b-147">Nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="86d9b-147">VM name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86d9b-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86d9b-148">CommonParameters</span></span>
<span data-ttu-id="86d9b-149">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86d9b-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86d9b-150">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86d9b-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86d9b-151">INPUT</span><span class="sxs-lookup"><span data-stu-id="86d9b-151">INPUTS</span></span>

### <span data-ttu-id="86d9b-152">Nessuno</span><span class="sxs-lookup"><span data-stu-id="86d9b-152">None</span></span>
## <span data-ttu-id="86d9b-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="86d9b-153">OUTPUTS</span></span>

### <span data-ttu-id="86d9b-154">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatus</span><span class="sxs-lookup"><span data-stu-id="86d9b-154">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatus</span></span>
## <span data-ttu-id="86d9b-155">NOTE</span><span class="sxs-lookup"><span data-stu-id="86d9b-155">NOTES</span></span>

## <span data-ttu-id="86d9b-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="86d9b-156">RELATED LINKS</span></span>
