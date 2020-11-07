---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 73E6DF02-7171-481B-966F-DECEC122A602
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/register-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
ms.openlocfilehash: 5dc2682597be6f05a65bafc38424139e9707578f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93685010"
---
# <span data-ttu-id="a3d97-101">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="a3d97-101">Register-AzAutomationDscNode</span></span>

## <span data-ttu-id="a3d97-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a3d97-102">SYNOPSIS</span></span>
<span data-ttu-id="a3d97-103">Registra una macchina virtuale di Azure come nodo DSC per un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="a3d97-103">Registers an Azure virtual machine as a DSC node for an Automation account.</span></span>

## <span data-ttu-id="a3d97-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a3d97-104">SYNTAX</span></span>

```
Register-AzAutomationDscNode -AzureVMName <String> [-NodeConfigurationName <String>]
 [-ConfigurationMode <String>] [-ConfigurationModeFrequencyMins <Int32>] [-RefreshFrequencyMins <Int32>]
 [-RebootNodeIfNeeded <Boolean>] [-ActionAfterReboot <String>] [-AllowModuleOverwrite <Boolean>]
 [-AzureVMResourceGroup <String>] [-AzureVMLocation <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3d97-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a3d97-105">DESCRIPTION</span></span>
<span data-ttu-id="a3d97-106">Il cmdlet **Register-AzAutomationDscNode** registra una macchina virtuale di Azure come nodo di configurazione dello stato (DSC) APS desiderato in un account di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="a3d97-106">The **Register-AzAutomationDscNode** cmdlet registers an Azure virtual machine as an APS Desired State Configuration (DSC) node in an Azure Automation account.</span></span>

## <span data-ttu-id="a3d97-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a3d97-107">EXAMPLES</span></span>

### <span data-ttu-id="a3d97-108">Esempio 1: registrare una macchina virtuale di Azure come nodo di Azure DSC</span><span class="sxs-lookup"><span data-stu-id="a3d97-108">Example 1: Register an Azure virtual machine as an Azure DSC node</span></span>
```
PS C:\>Register-AzAutomationDscNode -AutomationAccountName "Contoso17" -AzVMName "VirtualMachine01" -ResourceGroupName "ResourceGroup01"-NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="a3d97-109">Questo comando registra la macchina virtuale di Azure denominata VirtualMachine01 come nodo DSC nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="a3d97-109">This command registers the Azure virtual machine named VirtualMachine01 as a DSC node in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="a3d97-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a3d97-110">PARAMETERS</span></span>

### <span data-ttu-id="a3d97-111">-ActionAfterReboot</span><span class="sxs-lookup"><span data-stu-id="a3d97-111">-ActionAfterReboot</span></span>
<span data-ttu-id="a3d97-112">Specifica l'azione che la macchina virtuale prende dopo il riavvio.</span><span class="sxs-lookup"><span data-stu-id="a3d97-112">Specifies the action that the virtual machine takes after it restarts.</span></span>
<span data-ttu-id="a3d97-113">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="a3d97-113">Valid values are:</span></span> 
- <span data-ttu-id="a3d97-114">ContinueConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3d97-114">ContinueConfiguration</span></span> 
- <span data-ttu-id="a3d97-115">StopConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3d97-115">StopConfiguration</span></span>

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

### <span data-ttu-id="a3d97-116">-AllowModuleOverwrite</span><span class="sxs-lookup"><span data-stu-id="a3d97-116">-AllowModuleOverwrite</span></span>
<span data-ttu-id="a3d97-117">Specifica se le nuove configurazioni che questo nodo DSC Scarica dal server di pull di Azure Automation DSC sostituisce i moduli esistenti già presenti nel nodo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a3d97-117">Specifies whether new configurations that this DSC node downloads from the Azure Automation DSC pull server replace the existing modules already on the target node.</span></span>

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

### <span data-ttu-id="a3d97-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a3d97-118">-AutomationAccountName</span></span>
<span data-ttu-id="a3d97-119">Specifica il nome di un account di automazione in cui questo cmdlet registra una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a3d97-119">Specifies the name of an Automation account in which this cmdlet registers a virtual machine.</span></span>

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

### <span data-ttu-id="a3d97-120">-AzureVMLocation</span><span class="sxs-lookup"><span data-stu-id="a3d97-120">-AzureVMLocation</span></span>
<span data-ttu-id="a3d97-121">La posizione di Azure VM.</span><span class="sxs-lookup"><span data-stu-id="a3d97-121">The Azure VM location.</span></span>

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

### <span data-ttu-id="a3d97-122">-AzureVMName</span><span class="sxs-lookup"><span data-stu-id="a3d97-122">-AzureVMName</span></span>
<span data-ttu-id="a3d97-123">Nome della macchina virtuale di Azure da registrare per la gestione con Azure Automation DSC.</span><span class="sxs-lookup"><span data-stu-id="a3d97-123">The name of the Azure virtual machine to register for management with Azure Automation DSC.</span></span>

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

### <span data-ttu-id="a3d97-124">-AzureVMResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a3d97-124">-AzureVMResourceGroup</span></span>
<span data-ttu-id="a3d97-125">Nome del gruppo di risorse di Azure VM.</span><span class="sxs-lookup"><span data-stu-id="a3d97-125">The Azure VM resource group name.</span></span>

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

### <span data-ttu-id="a3d97-126">-ConfigurationMode</span><span class="sxs-lookup"><span data-stu-id="a3d97-126">-ConfigurationMode</span></span>
<span data-ttu-id="a3d97-127">Specifica la modalità di configurazione DSC.</span><span class="sxs-lookup"><span data-stu-id="a3d97-127">Specifies the DSC configuration mode.</span></span>
<span data-ttu-id="a3d97-128">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="a3d97-128">Valid values are:</span></span> 
- <span data-ttu-id="a3d97-129">ApplyAndMonitor</span><span class="sxs-lookup"><span data-stu-id="a3d97-129">ApplyAndMonitor</span></span> 
- <span data-ttu-id="a3d97-130">ApplyAndAutocorrect</span><span class="sxs-lookup"><span data-stu-id="a3d97-130">ApplyAndAutocorrect</span></span> 
- <span data-ttu-id="a3d97-131">ApplyOnly</span><span class="sxs-lookup"><span data-stu-id="a3d97-131">ApplyOnly</span></span>

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

### <span data-ttu-id="a3d97-132">-ConfigurationModeFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="a3d97-132">-ConfigurationModeFrequencyMins</span></span>
<span data-ttu-id="a3d97-133">Specifica la frequenza, in minuti, in cui l'applicazione in background di DSC tenta di implementare la configurazione corrente nel nodo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a3d97-133">Specifies the frequency, in minutes, at which the background application of DSC attempts to implement the current configuration on the target node.</span></span>

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

### <span data-ttu-id="a3d97-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3d97-134">-DefaultProfile</span></span>
<span data-ttu-id="a3d97-135">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a3d97-135">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a3d97-136">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="a3d97-136">-NodeConfigurationName</span></span>
<span data-ttu-id="a3d97-137">Specifica il nome della configurazione del nodo che questo cmdlet configura per la macchina virtuale per il pull da Azure Automation DSC.</span><span class="sxs-lookup"><span data-stu-id="a3d97-137">Specifies the name of the node configuration that this cmdlet configures the virtual machine to pull from Azure Automation DSC.</span></span>

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

### <span data-ttu-id="a3d97-138">-RebootNodeIfNeeded</span><span class="sxs-lookup"><span data-stu-id="a3d97-138">-RebootNodeIfNeeded</span></span>
<span data-ttu-id="a3d97-139">Specifica se riavviare la macchina virtuale, se necessario.</span><span class="sxs-lookup"><span data-stu-id="a3d97-139">Specifies whether to restart the virtual machine, if needed.</span></span>

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

### <span data-ttu-id="a3d97-140">-RefreshFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="a3d97-140">-RefreshFrequencyMins</span></span>
<span data-ttu-id="a3d97-141">Specifica la frequenza, in minuti, in cui il gestore configurazione locale contatta il server di pull di Azure Automation DSC per scaricare la configurazione più recente dei nodi.</span><span class="sxs-lookup"><span data-stu-id="a3d97-141">Specifies the frequency, in minutes, at which the local Configuration Manager contacts the Azure Automation DSC pull server to download the latest node configuration.</span></span>

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

### <span data-ttu-id="a3d97-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3d97-142">-ResourceGroupName</span></span>
<span data-ttu-id="a3d97-143">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a3d97-143">Specifies the name of a resource group.</span></span>
<span data-ttu-id="a3d97-144">L'account di automazione con cui questo cmdlet registra una macchina virtuale appartiene al gruppo di risorse specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="a3d97-144">The Automation account with which this cmdlet registers a virtual machine belongs to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a3d97-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3d97-145">CommonParameters</span></span>
<span data-ttu-id="a3d97-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3d97-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3d97-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3d97-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3d97-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a3d97-148">INPUTS</span></span>

### <span data-ttu-id="a3d97-149">System. String</span><span class="sxs-lookup"><span data-stu-id="a3d97-149">System.String</span></span>

### <span data-ttu-id="a3d97-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="a3d97-150">System.Int32</span></span>

### <span data-ttu-id="a3d97-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a3d97-151">System.Boolean</span></span>

## <span data-ttu-id="a3d97-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a3d97-152">OUTPUTS</span></span>

### <span data-ttu-id="a3d97-153">System. void</span><span class="sxs-lookup"><span data-stu-id="a3d97-153">System.Void</span></span>

## <span data-ttu-id="a3d97-154">Note</span><span class="sxs-lookup"><span data-stu-id="a3d97-154">NOTES</span></span>

## <span data-ttu-id="a3d97-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a3d97-155">RELATED LINKS</span></span>

[<span data-ttu-id="a3d97-156">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="a3d97-156">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="a3d97-157">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="a3d97-157">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)

[<span data-ttu-id="a3d97-158">Annullamento della registrazione-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="a3d97-158">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)


