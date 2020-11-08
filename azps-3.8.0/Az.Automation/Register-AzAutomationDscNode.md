---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 73E6DF02-7171-481B-966F-DECEC122A602
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/register-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
ms.openlocfilehash: e8367d4e291f3cd08cdb1020375cce1741a679c8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022907"
---
# <span data-ttu-id="6be27-101">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="6be27-101">Register-AzAutomationDscNode</span></span>

## <span data-ttu-id="6be27-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6be27-102">SYNOPSIS</span></span>
<span data-ttu-id="6be27-103">Registra una macchina virtuale di Azure che esegue Windows OS come nodo DSC per un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="6be27-103">Registers an Azure virtual machine running Windows OS as a DSC node for an Automation account.</span></span>

## <span data-ttu-id="6be27-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6be27-104">SYNTAX</span></span>

```
Register-AzAutomationDscNode -AzureVMName <String> [-NodeConfigurationName <String>]
 [-ConfigurationMode <String>] [-ConfigurationModeFrequencyMins <Int32>] [-RefreshFrequencyMins <Int32>]
 [-RebootNodeIfNeeded <Boolean>] [-ActionAfterReboot <String>] [-AllowModuleOverwrite <Boolean>]
 [-AzureVMResourceGroup <String>] [-AzureVMLocation <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6be27-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6be27-105">DESCRIPTION</span></span>
<span data-ttu-id="6be27-106">Il cmdlet **Register-AzAutomationDscNode** registra una macchina virtuale di Azure come nodo di configurazione dello stato (DSC) APS desiderato in un account di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="6be27-106">The **Register-AzAutomationDscNode** cmdlet registers an Azure virtual machine as an APS Desired State Configuration (DSC) node in an Azure Automation account.</span></span> <span data-ttu-id="6be27-107">Questo cmdlet registrerà solo le VM con sistema operativo Windows come nodo DSC di automazione per un account.</span><span class="sxs-lookup"><span data-stu-id="6be27-107">This cmdlet will only register VMs running Windows OS as an Automation DSC Node for an account.</span></span>

<span data-ttu-id="6be27-108">Se è necessario registrare un nodo in un account di automazione in un altro abbonamento, sarà necessario usare un modello ARM anziché i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6be27-108">If you need to register a node to an automation account in a different subscription, you will need to use an ARM template rather than cmdlets.</span></span> <span data-ttu-id="6be27-109">Per altre informazioni, vedere la [documentazione](https://docs.microsoft.com/en-us/azure/automation/automation-dsc-onboarding#registering-virtual-machines-across-azure-subscriptions) di Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="6be27-109">See the Azure Automation [documentation](https://docs.microsoft.com/en-us/azure/automation/automation-dsc-onboarding#registering-virtual-machines-across-azure-subscriptions) for more details.</span></span>

## <span data-ttu-id="6be27-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6be27-110">EXAMPLES</span></span>

### <span data-ttu-id="6be27-111">Esempio 1: registrare una macchina virtuale di Azure come nodo di Azure DSC</span><span class="sxs-lookup"><span data-stu-id="6be27-111">Example 1: Register an Azure virtual machine as an Azure DSC node</span></span>
```
PS C:\>Register-AzAutomationDscNode -AutomationAccountName "Contoso17" -AzureVMName "VirtualMachine01" -ResourceGroupName "ResourceGroup01"-NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="6be27-112">Questo comando registra la macchina virtuale di Azure denominata VirtualMachine01 come nodo DSC nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="6be27-112">This command registers the Azure virtual machine named VirtualMachine01 as a DSC node in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="6be27-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6be27-113">PARAMETERS</span></span>

### <span data-ttu-id="6be27-114">-ActionAfterReboot</span><span class="sxs-lookup"><span data-stu-id="6be27-114">-ActionAfterReboot</span></span>
<span data-ttu-id="6be27-115">Specifica l'azione che la macchina virtuale prende dopo il riavvio.</span><span class="sxs-lookup"><span data-stu-id="6be27-115">Specifies the action that the virtual machine takes after it restarts.</span></span>
<span data-ttu-id="6be27-116">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="6be27-116">Valid values are:</span></span> 
- <span data-ttu-id="6be27-117">ContinueConfiguration</span><span class="sxs-lookup"><span data-stu-id="6be27-117">ContinueConfiguration</span></span> 
- <span data-ttu-id="6be27-118">StopConfiguration</span><span class="sxs-lookup"><span data-stu-id="6be27-118">StopConfiguration</span></span>

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

### <span data-ttu-id="6be27-119">-AllowModuleOverwrite</span><span class="sxs-lookup"><span data-stu-id="6be27-119">-AllowModuleOverwrite</span></span>
<span data-ttu-id="6be27-120">Specifica se le nuove configurazioni che questo nodo DSC Scarica dal server di pull di Azure Automation DSC sostituisce i moduli esistenti già presenti nel nodo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="6be27-120">Specifies whether new configurations that this DSC node downloads from the Azure Automation DSC pull server replace the existing modules already on the target node.</span></span>

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

### <span data-ttu-id="6be27-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6be27-121">-AutomationAccountName</span></span>
<span data-ttu-id="6be27-122">Specifica il nome di un account di automazione in cui questo cmdlet registra una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6be27-122">Specifies the name of an Automation account in which this cmdlet registers a virtual machine.</span></span>

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

### <span data-ttu-id="6be27-123">-AzureVMLocation</span><span class="sxs-lookup"><span data-stu-id="6be27-123">-AzureVMLocation</span></span>
<span data-ttu-id="6be27-124">La posizione di Azure VM.</span><span class="sxs-lookup"><span data-stu-id="6be27-124">The Azure VM location.</span></span>

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

### <span data-ttu-id="6be27-125">-AzureVMName</span><span class="sxs-lookup"><span data-stu-id="6be27-125">-AzureVMName</span></span>
<span data-ttu-id="6be27-126">Nome della macchina virtuale di Azure da registrare per la gestione con Azure Automation DSC.</span><span class="sxs-lookup"><span data-stu-id="6be27-126">The name of the Azure virtual machine to register for management with Azure Automation DSC.</span></span>

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

### <span data-ttu-id="6be27-127">-AzureVMResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6be27-127">-AzureVMResourceGroup</span></span>
<span data-ttu-id="6be27-128">Nome del gruppo di risorse di Azure VM.</span><span class="sxs-lookup"><span data-stu-id="6be27-128">The Azure VM resource group name.</span></span>

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

### <span data-ttu-id="6be27-129">-ConfigurationMode</span><span class="sxs-lookup"><span data-stu-id="6be27-129">-ConfigurationMode</span></span>
<span data-ttu-id="6be27-130">Specifica la modalità di configurazione DSC.</span><span class="sxs-lookup"><span data-stu-id="6be27-130">Specifies the DSC configuration mode.</span></span>
<span data-ttu-id="6be27-131">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="6be27-131">Valid values are:</span></span> 
- <span data-ttu-id="6be27-132">ApplyAndMonitor</span><span class="sxs-lookup"><span data-stu-id="6be27-132">ApplyAndMonitor</span></span> 
- <span data-ttu-id="6be27-133">ApplyAndAutocorrect</span><span class="sxs-lookup"><span data-stu-id="6be27-133">ApplyAndAutocorrect</span></span> 
- <span data-ttu-id="6be27-134">ApplyOnly</span><span class="sxs-lookup"><span data-stu-id="6be27-134">ApplyOnly</span></span>

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

### <span data-ttu-id="6be27-135">-ConfigurationModeFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="6be27-135">-ConfigurationModeFrequencyMins</span></span>
<span data-ttu-id="6be27-136">Specifica la frequenza, in minuti, in cui l'applicazione in background di DSC tenta di implementare la configurazione corrente nel nodo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="6be27-136">Specifies the frequency, in minutes, at which the background application of DSC attempts to implement the current configuration on the target node.</span></span>

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

### <span data-ttu-id="6be27-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6be27-137">-DefaultProfile</span></span>
<span data-ttu-id="6be27-138">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6be27-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6be27-139">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="6be27-139">-NodeConfigurationName</span></span>
<span data-ttu-id="6be27-140">Specifica il nome della configurazione del nodo che questo cmdlet configura per la macchina virtuale per il pull da Azure Automation DSC.</span><span class="sxs-lookup"><span data-stu-id="6be27-140">Specifies the name of the node configuration that this cmdlet configures the virtual machine to pull from Azure Automation DSC.</span></span>

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

### <span data-ttu-id="6be27-141">-RebootNodeIfNeeded</span><span class="sxs-lookup"><span data-stu-id="6be27-141">-RebootNodeIfNeeded</span></span>
<span data-ttu-id="6be27-142">Specifica se riavviare la macchina virtuale, se necessario.</span><span class="sxs-lookup"><span data-stu-id="6be27-142">Specifies whether to restart the virtual machine, if needed.</span></span>

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

### <span data-ttu-id="6be27-143">-RefreshFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="6be27-143">-RefreshFrequencyMins</span></span>
<span data-ttu-id="6be27-144">Specifica la frequenza, in minuti, in cui il gestore configurazione locale contatta il server di pull di Azure Automation DSC per scaricare la configurazione più recente dei nodi.</span><span class="sxs-lookup"><span data-stu-id="6be27-144">Specifies the frequency, in minutes, at which the local Configuration Manager contacts the Azure Automation DSC pull server to download the latest node configuration.</span></span>

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

### <span data-ttu-id="6be27-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6be27-145">-ResourceGroupName</span></span>
<span data-ttu-id="6be27-146">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6be27-146">Specifies the name of a resource group.</span></span>
<span data-ttu-id="6be27-147">L'account di automazione con cui questo cmdlet registra una macchina virtuale appartiene al gruppo di risorse specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="6be27-147">The Automation account with which this cmdlet registers a virtual machine belongs to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="6be27-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6be27-148">CommonParameters</span></span>
<span data-ttu-id="6be27-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6be27-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6be27-150">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6be27-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6be27-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6be27-151">INPUTS</span></span>

### <span data-ttu-id="6be27-152">System. String</span><span class="sxs-lookup"><span data-stu-id="6be27-152">System.String</span></span>

### <span data-ttu-id="6be27-153">System. Int32</span><span class="sxs-lookup"><span data-stu-id="6be27-153">System.Int32</span></span>

### <span data-ttu-id="6be27-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6be27-154">System.Boolean</span></span>

## <span data-ttu-id="6be27-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6be27-155">OUTPUTS</span></span>

### <span data-ttu-id="6be27-156">System. void</span><span class="sxs-lookup"><span data-stu-id="6be27-156">System.Void</span></span>

## <span data-ttu-id="6be27-157">Note</span><span class="sxs-lookup"><span data-stu-id="6be27-157">NOTES</span></span>

## <span data-ttu-id="6be27-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6be27-158">RELATED LINKS</span></span>

[<span data-ttu-id="6be27-159">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="6be27-159">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="6be27-160">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="6be27-160">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)

[<span data-ttu-id="6be27-161">Annullamento della registrazione-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="6be27-161">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)


