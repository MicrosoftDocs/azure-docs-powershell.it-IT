---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 73E6DF02-7171-481B-966F-DECEC122A602
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/register-azurermautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRmAutomationDscNode.md
ms.openlocfilehash: 567ac6012465508fbaf03d603a79d2abb04ed6c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517636"
---
# <span data-ttu-id="a79c6-101">Register-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="a79c6-101">Register-AzureRmAutomationDscNode</span></span>

## <span data-ttu-id="a79c6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a79c6-102">SYNOPSIS</span></span>
<span data-ttu-id="a79c6-103">Registra una macchina virtuale di Azure come nodo DSC per un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="a79c6-103">Registers an Azure virtual machine as a DSC node for an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a79c6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a79c6-104">SYNTAX</span></span>

```
Register-AzureRmAutomationDscNode -AzureVMName <String> [-NodeConfigurationName <String>]
 [-ConfigurationMode <String>] [-ConfigurationModeFrequencyMins <Int32>] [-RefreshFrequencyMins <Int32>]
 [-RebootNodeIfNeeded <Boolean>] [-ActionAfterReboot <String>] [-AllowModuleOverwrite <Boolean>]
 [-AzureVMResourceGroup <String>] [-AzureVMLocation <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a79c6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a79c6-105">DESCRIPTION</span></span>
<span data-ttu-id="a79c6-106">Il cmdlet **Register-AzureRmAutomationDscNode** registra una macchina virtuale di Azure come nodo di configurazione dello stato (DSC) APS desiderato in un account di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="a79c6-106">The **Register-AzureRmAutomationDscNode** cmdlet registers an Azure virtual machine as an APS Desired State Configuration (DSC) node in an Azure Automation account.</span></span>

## <span data-ttu-id="a79c6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a79c6-107">EXAMPLES</span></span>

### <span data-ttu-id="a79c6-108">Esempio 1: registrare una macchina virtuale di Azure come nodo di Azure DSC</span><span class="sxs-lookup"><span data-stu-id="a79c6-108">Example 1: Register an Azure virtual machine as an Azure DSC node</span></span>
```
PS C:\>Register-AzureRmAutomationDscNode -AutomationAccountName "Contoso17" -AzureVMName "VirtualMachine01" -ResourceGroupName "ResourceGroup01"-NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="a79c6-109">Questo comando registra la macchina virtuale di Azure denominata VirtualMachine01 come nodo DSC nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="a79c6-109">This command registers the Azure virtual machine named VirtualMachine01 as a DSC node in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="a79c6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a79c6-110">PARAMETERS</span></span>

### <span data-ttu-id="a79c6-111">-ActionAfterReboot</span><span class="sxs-lookup"><span data-stu-id="a79c6-111">-ActionAfterReboot</span></span>
<span data-ttu-id="a79c6-112">Specifica l'azione che la macchina virtuale prende dopo il riavvio.</span><span class="sxs-lookup"><span data-stu-id="a79c6-112">Specifies the action that the virtual machine takes after it restarts.</span></span>
<span data-ttu-id="a79c6-113">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="a79c6-113">Valid values are:</span></span> 
- <span data-ttu-id="a79c6-114">ContinueConfiguration</span><span class="sxs-lookup"><span data-stu-id="a79c6-114">ContinueConfiguration</span></span> 
- <span data-ttu-id="a79c6-115">StopConfiguration</span><span class="sxs-lookup"><span data-stu-id="a79c6-115">StopConfiguration</span></span>

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

### <span data-ttu-id="a79c6-116">-AllowModuleOverwrite</span><span class="sxs-lookup"><span data-stu-id="a79c6-116">-AllowModuleOverwrite</span></span>
<span data-ttu-id="a79c6-117">Specifica se le nuove configurazioni che questo nodo DSC Scarica dal server di pull di Azure Automation DSC sostituisce i moduli esistenti già presenti nel nodo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a79c6-117">Specifies whether new configurations that this DSC node downloads from the Azure Automation DSC pull server replace the existing modules already on the target node.</span></span>

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

### <span data-ttu-id="a79c6-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a79c6-118">-AutomationAccountName</span></span>
<span data-ttu-id="a79c6-119">Specifica il nome di un account di automazione in cui questo cmdlet registra una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a79c6-119">Specifies the name of an Automation account in which this cmdlet registers a virtual machine.</span></span>

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

### <span data-ttu-id="a79c6-120">-AzureVMLocation</span><span class="sxs-lookup"><span data-stu-id="a79c6-120">-AzureVMLocation</span></span>
<span data-ttu-id="a79c6-121">Specifica la posizione in cui questo cmdlet registra una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a79c6-121">Specifies the location in which this cmdlet registers a virtual machine.</span></span>
<span data-ttu-id="a79c6-122">Per ottenere posizioni valide, usare il cmdlet Get-AzureRMLocation.</span><span class="sxs-lookup"><span data-stu-id="a79c6-122">To obtain valid locations, use the Get-AzureRMLocation cmdlet.</span></span>

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

### <span data-ttu-id="a79c6-123">-AzureVMName</span><span class="sxs-lookup"><span data-stu-id="a79c6-123">-AzureVMName</span></span>
<span data-ttu-id="a79c6-124">Specifica il nome della macchina virtuale di Azure che il cmdlet esegue la registrazione per la gestione.</span><span class="sxs-lookup"><span data-stu-id="a79c6-124">Specifies the name of the Azure virtual machine that this cmdlet registers for management.</span></span>

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

### <span data-ttu-id="a79c6-125">-AzureVMResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a79c6-125">-AzureVMResourceGroup</span></span>
<span data-ttu-id="a79c6-126">Specifica il nome del gruppo di risorse della macchina virtuale di Azure che questo cmdlet registra.</span><span class="sxs-lookup"><span data-stu-id="a79c6-126">Specifies the name of the resource group of the Azure virtual machine that this cmdlet registers.</span></span>

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

### <span data-ttu-id="a79c6-127">-ConfigurationMode</span><span class="sxs-lookup"><span data-stu-id="a79c6-127">-ConfigurationMode</span></span>
<span data-ttu-id="a79c6-128">Specifica la modalità di configurazione DSC.</span><span class="sxs-lookup"><span data-stu-id="a79c6-128">Specifies the DSC configuration mode.</span></span>
<span data-ttu-id="a79c6-129">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="a79c6-129">Valid values are:</span></span> 
- <span data-ttu-id="a79c6-130">ApplyAndMonitor</span><span class="sxs-lookup"><span data-stu-id="a79c6-130">ApplyAndMonitor</span></span> 
- <span data-ttu-id="a79c6-131">ApplyAndAutocorrect</span><span class="sxs-lookup"><span data-stu-id="a79c6-131">ApplyAndAutocorrect</span></span> 
- <span data-ttu-id="a79c6-132">ApplyOnly</span><span class="sxs-lookup"><span data-stu-id="a79c6-132">ApplyOnly</span></span>

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

### <span data-ttu-id="a79c6-133">-ConfigurationModeFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="a79c6-133">-ConfigurationModeFrequencyMins</span></span>
<span data-ttu-id="a79c6-134">Specifica la frequenza, in minuti, in cui l'applicazione in background di DSC tenta di implementare la configurazione corrente nel nodo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a79c6-134">Specifies the frequency, in minutes, at which the background application of DSC attempts to implement the current configuration on the target node.</span></span>

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

### <span data-ttu-id="a79c6-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a79c6-135">-DefaultProfile</span></span>
<span data-ttu-id="a79c6-136">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a79c6-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a79c6-137">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="a79c6-137">-NodeConfigurationName</span></span>
<span data-ttu-id="a79c6-138">Specifica il nome della configurazione del nodo che questo cmdlet configura per la macchina virtuale per il pull da Azure Automation DSC.</span><span class="sxs-lookup"><span data-stu-id="a79c6-138">Specifies the name of the node configuration that this cmdlet configures the virtual machine to pull from Azure Automation DSC.</span></span>

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

### <span data-ttu-id="a79c6-139">-RebootNodeIfNeeded</span><span class="sxs-lookup"><span data-stu-id="a79c6-139">-RebootNodeIfNeeded</span></span>
<span data-ttu-id="a79c6-140">Specifica se riavviare la macchina virtuale, se necessario.</span><span class="sxs-lookup"><span data-stu-id="a79c6-140">Specifies whether to restart the virtual machine, if needed.</span></span>

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

### <span data-ttu-id="a79c6-141">-RefreshFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="a79c6-141">-RefreshFrequencyMins</span></span>
<span data-ttu-id="a79c6-142">Specifica la frequenza, in minuti, in cui il gestore configurazione locale contatta il server di pull di Azure Automation DSC per scaricare la configurazione più recente dei nodi.</span><span class="sxs-lookup"><span data-stu-id="a79c6-142">Specifies the frequency, in minutes, at which the local Configuration Manager contacts the Azure Automation DSC pull server to download the latest node configuration.</span></span>

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

### <span data-ttu-id="a79c6-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a79c6-143">-ResourceGroupName</span></span>
<span data-ttu-id="a79c6-144">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a79c6-144">Specifies the name of a resource group.</span></span>
<span data-ttu-id="a79c6-145">L'account di automazione con cui questo cmdlet registra una macchina virtuale appartiene al gruppo di risorse specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="a79c6-145">The Automation account with which this cmdlet registers a virtual machine belongs to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a79c6-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a79c6-146">CommonParameters</span></span>
<span data-ttu-id="a79c6-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a79c6-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a79c6-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a79c6-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a79c6-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a79c6-149">INPUTS</span></span>

### <span data-ttu-id="a79c6-150">System. String</span><span class="sxs-lookup"><span data-stu-id="a79c6-150">System.String</span></span>

### <span data-ttu-id="a79c6-151">System. Int32</span><span class="sxs-lookup"><span data-stu-id="a79c6-151">System.Int32</span></span>

### <span data-ttu-id="a79c6-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a79c6-152">System.Boolean</span></span>

## <span data-ttu-id="a79c6-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a79c6-153">OUTPUTS</span></span>

### <span data-ttu-id="a79c6-154">System. void</span><span class="sxs-lookup"><span data-stu-id="a79c6-154">System.Void</span></span>

## <span data-ttu-id="a79c6-155">Note</span><span class="sxs-lookup"><span data-stu-id="a79c6-155">NOTES</span></span>

## <span data-ttu-id="a79c6-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a79c6-156">RELATED LINKS</span></span>

[<span data-ttu-id="a79c6-157">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="a79c6-157">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="a79c6-158">Set-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="a79c6-158">Set-AzureRmAutomationDscNode</span></span>](./Set-AzureRmAutomationDscNode.md)

[<span data-ttu-id="a79c6-159">Annullamento della registrazione-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="a79c6-159">Unregister-AzureRmAutomationDscNode</span></span>](./Unregister-AzureRmAutomationDscNode.md)


