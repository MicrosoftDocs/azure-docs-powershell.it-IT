---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 73E6DF02-7171-481B-966F-DECEC122A602
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/register-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
ms.openlocfilehash: e8367d4e291f3cd08cdb1020375cce1741a679c8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182166"
---
# <span data-ttu-id="f93cb-101">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="f93cb-101">Register-AzAutomationDscNode</span></span>

## <span data-ttu-id="f93cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f93cb-102">SYNOPSIS</span></span>
<span data-ttu-id="f93cb-103">Registra una macchina virtuale di Azure che esegue Windows OS come nodo DSC per un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="f93cb-103">Registers an Azure virtual machine running Windows OS as a DSC node for an Automation account.</span></span>

## <span data-ttu-id="f93cb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f93cb-104">SYNTAX</span></span>

```
Register-AzAutomationDscNode -AzureVMName <String> [-NodeConfigurationName <String>]
 [-ConfigurationMode <String>] [-ConfigurationModeFrequencyMins <Int32>] [-RefreshFrequencyMins <Int32>]
 [-RebootNodeIfNeeded <Boolean>] [-ActionAfterReboot <String>] [-AllowModuleOverwrite <Boolean>]
 [-AzureVMResourceGroup <String>] [-AzureVMLocation <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f93cb-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f93cb-105">DESCRIPTION</span></span>
<span data-ttu-id="f93cb-106">Il cmdlet **Register-AzAutomationDscNode** registra una macchina virtuale di Azure come nodo APS Desired State Configuration (DSC) in un account di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f93cb-106">The **Register-AzAutomationDscNode** cmdlet registers an Azure virtual machine as an APS Desired State Configuration (DSC) node in an Azure Automation account.</span></span> <span data-ttu-id="f93cb-107">Questo cmdlet registrerà solo le macchine virtuali che eseguono Windows OS come nodo DSC di automazione per un account.</span><span class="sxs-lookup"><span data-stu-id="f93cb-107">This cmdlet will only register VMs running Windows OS as an Automation DSC Node for an account.</span></span>

<span data-ttu-id="f93cb-108">Se è necessario registrare un nodo in un account di automazione in un abbonamento diverso, è necessario usare un modello di ARM invece dei cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f93cb-108">If you need to register a node to an automation account in a different subscription, you will need to use an ARM template rather than cmdlets.</span></span> <span data-ttu-id="f93cb-109">Per altre informazioni, vedere la [documentazione](https://docs.microsoft.com/en-us/azure/automation/automation-dsc-onboarding#registering-virtual-machines-across-azure-subscriptions) sull'automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f93cb-109">See the Azure Automation [documentation](https://docs.microsoft.com/en-us/azure/automation/automation-dsc-onboarding#registering-virtual-machines-across-azure-subscriptions) for more details.</span></span>

## <span data-ttu-id="f93cb-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f93cb-110">EXAMPLES</span></span>

### <span data-ttu-id="f93cb-111">Esempio 1: Registrare una macchina virtuale di Azure come nodo DSC di Azure</span><span class="sxs-lookup"><span data-stu-id="f93cb-111">Example 1: Register an Azure virtual machine as an Azure DSC node</span></span>
```
PS C:\>Register-AzAutomationDscNode -AutomationAccountName "Contoso17" -AzureVMName "VirtualMachine01" -ResourceGroupName "ResourceGroup01"-NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="f93cb-112">Questo comando registra la macchina virtuale di Azure denominata VirtualMachine01 come nodo DSC nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f93cb-112">This command registers the Azure virtual machine named VirtualMachine01 as a DSC node in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="f93cb-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f93cb-113">PARAMETERS</span></span>

### <span data-ttu-id="f93cb-114">-ActionAfterReboot</span><span class="sxs-lookup"><span data-stu-id="f93cb-114">-ActionAfterReboot</span></span>
<span data-ttu-id="f93cb-115">Specifica l'azione eseguita dalla macchina virtuale dopo il riavvio.</span><span class="sxs-lookup"><span data-stu-id="f93cb-115">Specifies the action that the virtual machine takes after it restarts.</span></span>
<span data-ttu-id="f93cb-116">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="f93cb-116">Valid values are:</span></span> 
- <span data-ttu-id="f93cb-117">ContinueConfiguration</span><span class="sxs-lookup"><span data-stu-id="f93cb-117">ContinueConfiguration</span></span> 
- <span data-ttu-id="f93cb-118">StopConfiguration</span><span class="sxs-lookup"><span data-stu-id="f93cb-118">StopConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ContinueConfiguration, StopConfiguration

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f93cb-119">-AllowModuleOverwrite</span><span class="sxs-lookup"><span data-stu-id="f93cb-119">-AllowModuleOverwrite</span></span>
<span data-ttu-id="f93cb-120">Specifica se le nuove configurazioni scaricate da questo nodo DSC dal server di pull DSC di automazione di Azure sostituiscono i moduli esistenti già presenti nel nodo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f93cb-120">Specifies whether new configurations that this DSC node downloads from the Azure Automation DSC pull server replace the existing modules already on the target node.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f93cb-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f93cb-121">-AutomationAccountName</span></span>
<span data-ttu-id="f93cb-122">Specifica il nome di un account di automazione in cui questo cmdlet registra una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f93cb-122">Specifies the name of an Automation account in which this cmdlet registers a virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f93cb-123">-AzureVMLocation</span><span class="sxs-lookup"><span data-stu-id="f93cb-123">-AzureVMLocation</span></span>
<span data-ttu-id="f93cb-124">Posizione della macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="f93cb-124">The Azure VM location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f93cb-125">-AzureVMName</span><span class="sxs-lookup"><span data-stu-id="f93cb-125">-AzureVMName</span></span>
<span data-ttu-id="f93cb-126">Nome della macchina virtuale di Azure da registrare per la gestione con DSC di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f93cb-126">The name of the Azure virtual machine to register for management with Azure Automation DSC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f93cb-127">-AzureVMResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f93cb-127">-AzureVMResourceGroup</span></span>
<span data-ttu-id="f93cb-128">Nome del gruppo di risorse di Azure VM.</span><span class="sxs-lookup"><span data-stu-id="f93cb-128">The Azure VM resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f93cb-129">-ConfigurationMode</span><span class="sxs-lookup"><span data-stu-id="f93cb-129">-ConfigurationMode</span></span>
<span data-ttu-id="f93cb-130">Specifica la modalità di configurazione DSC.</span><span class="sxs-lookup"><span data-stu-id="f93cb-130">Specifies the DSC configuration mode.</span></span>
<span data-ttu-id="f93cb-131">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="f93cb-131">Valid values are:</span></span> 
- <span data-ttu-id="f93cb-132">ApplyAndMonitor</span><span class="sxs-lookup"><span data-stu-id="f93cb-132">ApplyAndMonitor</span></span> 
- <span data-ttu-id="f93cb-133">ApplyAndAutocorrect</span><span class="sxs-lookup"><span data-stu-id="f93cb-133">ApplyAndAutocorrect</span></span> 
- <span data-ttu-id="f93cb-134">ApplyOnly</span><span class="sxs-lookup"><span data-stu-id="f93cb-134">ApplyOnly</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ApplyAndMonitor, ApplyAndAutocorrect, ApplyOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f93cb-135">-ConfigurationModeFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="f93cb-135">-ConfigurationModeFrequencyMins</span></span>
<span data-ttu-id="f93cb-136">Specifica la frequenza in minuti con cui l'applicazione in background di DSC tenta di implementare la configurazione corrente nel nodo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f93cb-136">Specifies the frequency, in minutes, at which the background application of DSC attempts to implement the current configuration on the target node.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f93cb-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f93cb-137">-DefaultProfile</span></span>
<span data-ttu-id="f93cb-138">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="f93cb-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f93cb-139">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="f93cb-139">-NodeConfigurationName</span></span>
<span data-ttu-id="f93cb-140">Specifica il nome della configurazione del nodo che questo cmdlet configura la macchina virtuale per il pull dal DSC di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f93cb-140">Specifies the name of the node configuration that this cmdlet configures the virtual machine to pull from Azure Automation DSC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f93cb-141">-RebootNodeIfNeeded</span><span class="sxs-lookup"><span data-stu-id="f93cb-141">-RebootNodeIfNeeded</span></span>
<span data-ttu-id="f93cb-142">Specifica se riavviare la macchina virtuale, se necessario.</span><span class="sxs-lookup"><span data-stu-id="f93cb-142">Specifies whether to restart the virtual machine, if needed.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f93cb-143">-RefreshFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="f93cb-143">-RefreshFrequencyMins</span></span>
<span data-ttu-id="f93cb-144">Specifica la frequenza in minuti con cui Gestione configurazione locale contatta il server pull DSC di Automazione di Azure per scaricare la configurazione del nodo più recente.</span><span class="sxs-lookup"><span data-stu-id="f93cb-144">Specifies the frequency, in minutes, at which the local Configuration Manager contacts the Azure Automation DSC pull server to download the latest node configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f93cb-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f93cb-145">-ResourceGroupName</span></span>
<span data-ttu-id="f93cb-146">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f93cb-146">Specifies the name of a resource group.</span></span>
<span data-ttu-id="f93cb-147">L'account di automazione con cui questo cmdlet registra una macchina virtuale appartiene al gruppo di risorse specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="f93cb-147">The Automation account with which this cmdlet registers a virtual machine belongs to the resource group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f93cb-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f93cb-148">CommonParameters</span></span>
<span data-ttu-id="f93cb-149">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f93cb-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f93cb-150">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f93cb-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f93cb-151">INPUT</span><span class="sxs-lookup"><span data-stu-id="f93cb-151">INPUTS</span></span>

### <span data-ttu-id="f93cb-152">System.String</span><span class="sxs-lookup"><span data-stu-id="f93cb-152">System.String</span></span>

### <span data-ttu-id="f93cb-153">System.Int32</span><span class="sxs-lookup"><span data-stu-id="f93cb-153">System.Int32</span></span>

### <span data-ttu-id="f93cb-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f93cb-154">System.Boolean</span></span>

## <span data-ttu-id="f93cb-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f93cb-155">OUTPUTS</span></span>

### <span data-ttu-id="f93cb-156">System.Void</span><span class="sxs-lookup"><span data-stu-id="f93cb-156">System.Void</span></span>

## <span data-ttu-id="f93cb-157">NOTE</span><span class="sxs-lookup"><span data-stu-id="f93cb-157">NOTES</span></span>

## <span data-ttu-id="f93cb-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f93cb-158">RELATED LINKS</span></span>

[<span data-ttu-id="f93cb-159">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="f93cb-159">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="f93cb-160">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="f93cb-160">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)

[<span data-ttu-id="f93cb-161">Unregister-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="f93cb-161">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)


