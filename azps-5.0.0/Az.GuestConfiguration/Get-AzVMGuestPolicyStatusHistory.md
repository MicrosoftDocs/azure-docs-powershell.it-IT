---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-azvmguestpolicystatushistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
ms.openlocfilehash: 929bc417cf4b84800635b85e7f503972509aa7fc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193356"
---
# <span data-ttu-id="f2dab-101">Get-AzVMGuestPolicyStatusHistory</span><span class="sxs-lookup"><span data-stu-id="f2dab-101">Get-AzVMGuestPolicyStatusHistory</span></span>

## <span data-ttu-id="f2dab-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f2dab-102">SYNOPSIS</span></span>
<span data-ttu-id="f2dab-103">Ottiene la cronologia dello stato di conformità dei criteri di configurazione Guest per un'iniziativa di tipo "Guest Configuration" assegnata a una VM.</span><span class="sxs-lookup"><span data-stu-id="f2dab-103">Gets guest configuration policy compliance status history for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="f2dab-104">Un'iniziativa è un criterio di tipo definizione "iniziativa".</span><span class="sxs-lookup"><span data-stu-id="f2dab-104">An initiative is a policy of definition type "Initiative".</span></span>

## <span data-ttu-id="f2dab-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f2dab-105">SYNTAX</span></span>

### <span data-ttu-id="f2dab-106">InitiativeNameScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f2dab-106">InitiativeNameScope (Default)</span></span>
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2dab-107">InitiativeIdScope</span><span class="sxs-lookup"><span data-stu-id="f2dab-107">InitiativeIdScope</span></span>
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [[-InitiativeId] <String>]
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2dab-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f2dab-108">DESCRIPTION</span></span>
<span data-ttu-id="f2dab-109">Il cmdlet Get-AzVMGuestPolicyStatusHistory ottiene la cronologia dello stato di conformità dei criteri di configurazione Guest per un'iniziativa di tipo "configurazione Guest" assegnata a una VM.</span><span class="sxs-lookup"><span data-stu-id="f2dab-109">The Get-AzVMGuestPolicyStatusHistory cmdlet gets compliance status history of guest configuration policies for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="f2dab-110">Un'iniziativa è un criterio di tipo definizione "iniziativa".</span><span class="sxs-lookup"><span data-stu-id="f2dab-110">An initiative is a policy of definition type "Initiative".</span></span>
<span data-ttu-id="f2dab-111">USA Get-AzVMGuestPolicyStatus cmdlet per ottenere informazioni dettagliate su un singolo stato di conformità usando ReportId che puoi trovare nell'output del cmdlet Get-AzVMGuestPolicyStatusHistory.</span><span class="sxs-lookup"><span data-stu-id="f2dab-111">Use Get-AzVMGuestPolicyStatus cmdlet to get details of a single compliance status using ReportId that can be found in output of Get-AzVMGuestPolicyStatusHistory cmdlet.</span></span>

## <span data-ttu-id="f2dab-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f2dab-112">EXAMPLES</span></span>

### <span data-ttu-id="f2dab-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f2dab-113">Example 1</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af" -ShowOnlyChange
```

<span data-ttu-id="f2dab-114">Ottiene la cronologia dello stato di conformità per iniziativa ID. ShowOnlyChange l'opzione Mostra solo le modifiche dello stato cronologico.</span><span class="sxs-lookup"><span data-stu-id="f2dab-114">Gets compliance status history by initiative Id. ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="f2dab-115">Ignora gli Stati che non sono stati modificati tra due controlli di conformità.</span><span class="sxs-lookup"><span data-stu-id="f2dab-115">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="f2dab-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f2dab-116">Example 2</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17" -ShowOnlyChange
```

<span data-ttu-id="f2dab-117">Ottiene la cronologia dello stato di conformità per nome dell'iniziativa.</span><span class="sxs-lookup"><span data-stu-id="f2dab-117">Gets compliance status history by initiative name.</span></span>
<span data-ttu-id="f2dab-118">L'opzione ShowOnlyChange Mostra solo le modifiche dello stato cronologico.</span><span class="sxs-lookup"><span data-stu-id="f2dab-118">ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="f2dab-119">Ignora gli Stati che non sono stati modificati tra due controlli di conformità.</span><span class="sxs-lookup"><span data-stu-id="f2dab-119">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="f2dab-120">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="f2dab-120">Example 3</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -ShowOnlyChange
```

<span data-ttu-id="f2dab-121">Ottiene la cronologia dello stato di conformità per tutti i criteri di configurazione guest assegnati alla VM.</span><span class="sxs-lookup"><span data-stu-id="f2dab-121">Gets compliance status history for all guest configuration policies assigned to the VM.</span></span>
<span data-ttu-id="f2dab-122">L'opzione ShowOnlyChange Mostra solo le modifiche dello stato cronologico.</span><span class="sxs-lookup"><span data-stu-id="f2dab-122">ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="f2dab-123">Ignora gli Stati che non sono stati modificati tra due controlli di conformità.</span><span class="sxs-lookup"><span data-stu-id="f2dab-123">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="f2dab-124">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="f2dab-124">Example 4</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

<span data-ttu-id="f2dab-125">Ottiene la cronologia dello stato di conformità per ID iniziativa.</span><span class="sxs-lookup"><span data-stu-id="f2dab-125">Gets compliance status history by initiative Id.</span></span>

### <span data-ttu-id="f2dab-126">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="f2dab-126">Example 5</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

<span data-ttu-id="f2dab-127">Ottiene la cronologia dello stato di conformità per nome dell'iniziativa.</span><span class="sxs-lookup"><span data-stu-id="f2dab-127">Gets compliance status history by initiative name.</span></span>

### <span data-ttu-id="f2dab-128">Esempio 6</span><span class="sxs-lookup"><span data-stu-id="f2dab-128">Example 6</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```
<span data-ttu-id="f2dab-129">Ottiene la cronologia dello stato di conformità per tutti i criteri di configurazione guest assegnati alla VM.</span><span class="sxs-lookup"><span data-stu-id="f2dab-129">Gets compliance status history for all guest configuration policies assigned to the VM.</span></span>

### <span data-ttu-id="f2dab-130">Esempio 7</span><span class="sxs-lookup"><span data-stu-id="f2dab-130">Example 7</span></span>
```powershell
PS C:\>$x = Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
PS C:\>$x[10].ReportId
/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac
PS C:\> Get-AzVMGuestPolicyStatus -ReportId $x[10].ReportId
```

<span data-ttu-id="f2dab-131">Ottenere lo stato dei criteri di configurazione Guest in ReportId.</span><span class="sxs-lookup"><span data-stu-id="f2dab-131">Get guest configuration policy status by ReportId.</span></span>
<span data-ttu-id="f2dab-132">ReportId è la proprietà ReportId che si trova nei risultati di Get-AzVMGuestPolicyStatusHistory.</span><span class="sxs-lookup"><span data-stu-id="f2dab-132">The ReportId is the ReportId property that can be found in the results of Get-AzVMGuestPolicyStatusHistory.</span></span> <span data-ttu-id="f2dab-133">(fare riferimento ad altri esempi)</span><span class="sxs-lookup"><span data-stu-id="f2dab-133">(please refer other examples)</span></span>

## <span data-ttu-id="f2dab-134">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f2dab-134">PARAMETERS</span></span>

### <span data-ttu-id="f2dab-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2dab-135">-DefaultProfile</span></span>
<span data-ttu-id="f2dab-136">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f2dab-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2dab-137">-InitiativeId</span><span class="sxs-lookup"><span data-stu-id="f2dab-137">-InitiativeId</span></span>
<span data-ttu-id="f2dab-138">ID definizione di un criterio in cui il tipo di definizione è Initiative e Category è la configurazione Guest</span><span class="sxs-lookup"><span data-stu-id="f2dab-138">Definition Id of a policy where definition type is Initiative and category is Guest Configuration</span></span>

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

### <span data-ttu-id="f2dab-139">-Initiativename</span><span class="sxs-lookup"><span data-stu-id="f2dab-139">-InitiativeName</span></span>
<span data-ttu-id="f2dab-140">Nome di un criterio in cui il tipo di definizione è Initiative e Category è la configurazione Guest</span><span class="sxs-lookup"><span data-stu-id="f2dab-140">Name of a policy where definition type is Initiative and category is Guest Configuration</span></span>

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

### <span data-ttu-id="f2dab-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2dab-141">-ResourceGroupName</span></span>
<span data-ttu-id="f2dab-142">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f2dab-142">Resource group name.</span></span>

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

### <span data-ttu-id="f2dab-143">-ShowOnlyChange</span><span class="sxs-lookup"><span data-stu-id="f2dab-143">-ShowOnlyChange</span></span>
<span data-ttu-id="f2dab-144">Mostra le modifiche dello stato cronologico solo per i criteri di configurazione Guest.</span><span class="sxs-lookup"><span data-stu-id="f2dab-144">Shows historical status changes only for guest configuration policies.</span></span>
<span data-ttu-id="f2dab-145">Ignora gli Stati che non sono stati modificati tra due esecuzioni di controllo dello stato di conformità.</span><span class="sxs-lookup"><span data-stu-id="f2dab-145">Skips statuses that have not changed between two compliance status audit runs.</span></span>

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

### <span data-ttu-id="f2dab-146">-VMName</span><span class="sxs-lookup"><span data-stu-id="f2dab-146">-VMName</span></span>
<span data-ttu-id="f2dab-147">Nome VM.</span><span class="sxs-lookup"><span data-stu-id="f2dab-147">VM name.</span></span>

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

### <span data-ttu-id="f2dab-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2dab-148">CommonParameters</span></span>
<span data-ttu-id="f2dab-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2dab-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2dab-150">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2dab-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2dab-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f2dab-151">INPUTS</span></span>

### <span data-ttu-id="f2dab-152">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f2dab-152">None</span></span>
## <span data-ttu-id="f2dab-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f2dab-153">OUTPUTS</span></span>

### <span data-ttu-id="f2dab-154">Microsoft. Azure. Commands. GuestConfiguration. Models. PolicyStatus</span><span class="sxs-lookup"><span data-stu-id="f2dab-154">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatus</span></span>
## <span data-ttu-id="f2dab-155">Note</span><span class="sxs-lookup"><span data-stu-id="f2dab-155">NOTES</span></span>

## <span data-ttu-id="f2dab-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f2dab-156">RELATED LINKS</span></span>
