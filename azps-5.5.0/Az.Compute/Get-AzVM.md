---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVM.md
ms.openlocfilehash: f1103e8fc7ed9646aa6b91bc0336e331f7ada990
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181718"
---
# <span data-ttu-id="25f15-101">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="25f15-101">Get-AzVM</span></span>

## <span data-ttu-id="25f15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25f15-102">SYNOPSIS</span></span>
<span data-ttu-id="25f15-103">Ottiene le proprietà di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="25f15-103">Gets the properties of a virtual machine.</span></span>

## <span data-ttu-id="25f15-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="25f15-104">SYNTAX</span></span>

### <span data-ttu-id="25f15-105">DefaultParamSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="25f15-105">DefaultParamSet (Default)</span></span>
```
Get-AzVM [[-ResourceGroupName] <String>] [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25f15-106">GetVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="25f15-106">GetVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25f15-107">ListLocationVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="25f15-107">ListLocationVirtualMachinesParamSet</span></span>
```
Get-AzVM -Location <String> [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25f15-108">ListNextLinkVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="25f15-108">ListNextLinkVirtualMachinesParamSet</span></span>
```
Get-AzVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25f15-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="25f15-109">DESCRIPTION</span></span>
<span data-ttu-id="25f15-110">Il **cmdlet Get-AzVM** ottiene la visualizzazione del modello o la visualizzazione dell'istanza di una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="25f15-110">The **Get-AzVM** cmdlet gets the model view or the instance view of an Azure virtual machine.</span></span>
<span data-ttu-id="25f15-111">La visualizzazione modello rappresenta le proprietà specificate dall'utente della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="25f15-111">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="25f15-112">La visualizzazione dell'istanza è lo stato a livello di istanza della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="25f15-112">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="25f15-113">Specificare il *parametro Status* per ottenere la visualizzazione dell'istanza di una macchina virtuale invece della visualizzazione modello, che è l'impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="25f15-113">Specify the *Status* parameter to get the instance view of a virtual machine instead of the model view which is the default.</span></span>

## <span data-ttu-id="25f15-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="25f15-114">EXAMPLES</span></span>

### <span data-ttu-id="25f15-115">Esempio 1: Ottenere le proprietà della visualizzazione modello e istanza</span><span class="sxs-lookup"><span data-stu-id="25f15-115">Example 1: Get model and instance view properties</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"

ResourceGroupName        : ResourceGroup11
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/M
icrosoft.Compute/virtualMachines/VirtualMachine07
VmId                     : 00000000-0000-0000-0000-000000000000
Name                     : VirtualMachine07
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {"creationSource":"acs-VirtualMachine07"}
AvailabilitySetReference : {Id}
DiagnosticsProfile       : {BootDiagnostics}
Extensions               : {linuxdiagnostic, waitforleader}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, LinuxConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
```

<span data-ttu-id="25f15-116">Questo comando ottiene le proprietà della visualizzazione modello e della visualizzazione istanza della macchina virtuale denominata VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="25f15-116">This command gets the model view and instance view properties of the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="25f15-117">Esempio 2: Ottenere le proprietà della visualizzazione istanza</span><span class="sxs-lookup"><span data-stu-id="25f15-117">Example 2: Get instance view properties</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status

ResourceGroupName       : ResourceGroup11
Name                    : VirtualMachine07
Disks[0]                :
  Name                  : VirtualMachine07-osdisk
  Statuses[0]           :
    Code                : ProvisioningState/succeeded
    Level               : Info
    DisplayStatus       : Provisioning succeeded
    Time                : 3/1/2019 12:59:30 AM
Extensions[0]           :
  Name                  : linuxdiagnostic
  Type                  : Microsoft.OSTCExtensions.LinuxDiagnostic
  TypeHandlerVersion    : 2.3.9029
  Statuses[0]           :
    Code                : ProvisioningState/succeeded
    Level               : Info
    DisplayStatus       : Provisioning succeeded
    Message             : Invalid config settings given: Empty storageAccountName. Install will proceed, but enable
can't proceed, in which case it's still considered a success as it's an external error.
Extensions[1]           :
  Name                  : waitforleader
  Type                  : Microsoft.OSTCExtensions.CustomScriptForLinux
  TypeHandlerVersion    : 1.5.4
  Statuses[0]           :
    Code                : ProvisioningState/succeeded
    Level               : Info
    DisplayStatus       : Provisioning succeeded
    Message             : Command is finished.
---stdout---
waiting for leader.mesos
waiting for leader.mesos
waiting for leader.mesos
waiting for leader.mesos
waiting for leader.mesos
waiting for leader.mesos
PING leader.mesos (xxx.xx.x.x) 56(84) bytes of data.
64 bytes from xxx.xx.x.x: icmp_seq=1 ttl=64 time=0.022 ms

--- leader.mesos ping statistics ---
1 packets transmitted, 1 received, 0% packet loss, time 0ms
rtt min/avg/max/mdev = 0.022/0.022/0.022/0.000 ms
leader.mesos up

---errout---
ping: unknown host leader.mesos
ping: unknown host leader.mesos
ping: unknown host leader.mesos
ping: unknown host leader.mesos
ping: unknown host leader.mesos
ping: unknown host leader.mesos


PlatformFaultDomain     : 0
PlatformUpdateDomain    : 0
VMAgent                 :
  VmAgentVersion        : 2.2.37
  ExtensionHandlers[0]  :
    Type                : Microsoft.OSTCExtensions.LinuxDiagnostic
    TypeHandlerVersion  : 2.3.9029
    Status              :
      Code              : ProvisioningState/succeeded
      Level             : Info
      DisplayStatus     : Ready
      Message           : Plugin enabled
  ExtensionHandlers[1]  :
    Type                : Microsoft.OSTCExtensions.CustomScriptForLinux
    TypeHandlerVersion  : 1.5.4
    Status              :
      Code              : ProvisioningState/succeeded
      Level             : Info
      DisplayStatus     : Ready
      Message           : Plugin enabled
  Statuses[0]           :
    Code                : ProvisioningState/succeeded
    Level               : Info
    DisplayStatus       : Ready
    Message             : Guest Agent is running
    Time                : 3/1/2019 2:04:12 AM
Statuses[0]             :
  Code                  : ProvisioningState/succeeded
  Level                 : Info
  DisplayStatus         : Provisioning succeeded
  Time                  : 3/1/2019 1:01:57 AM
Statuses[1]             :
  Code                  : PowerState/running
  Level                 : Info
  DisplayStatus         : VM running
```

<span data-ttu-id="25f15-118">Questo comando recupera le proprietà della macchina virtuale denominata VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="25f15-118">This command gets properties of the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="25f15-119">Questo comando specifica il *parametro Status.*</span><span class="sxs-lookup"><span data-stu-id="25f15-119">This command specifies the *Status* parameter.</span></span>
<span data-ttu-id="25f15-120">Di conseguenza, il comando ottiene solo le proprietà della visualizzazione istanza.</span><span class="sxs-lookup"><span data-stu-id="25f15-120">Therefore, the command gets only the instance view properties.</span></span>

### <span data-ttu-id="25f15-121">Esempio 3: Ottenere le proprietà per tutte le macchine virtuali in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="25f15-121">Example 3: Get properties for all virtual machines in a resource group</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11"

ResourceGroupName    Name       Location          VmSize  OsType            NIC
-----------------    ----       --------          ------  ------            ---
ResourceGroup11     test1         eastus Standard_DS1_v2 Windows          test1
ResourceGroup11     test2         westus Standard_DS1_v2 Windows          test2
ResourceGroup11     test3         eastus Standard_DS1_v2 Windows          test3
```

<span data-ttu-id="25f15-122">Questo comando recupera le proprietà per tutte le macchine virtuali nel gruppo di risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="25f15-122">This command gets properties for all the virtual machines in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="25f15-123">Esempio 4: Ottenere tutte le macchine virtuali nell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="25f15-123">Example 4: Get all virtual machines in your subscription</span></span>
```
PS C:\> Get-AzVM

ResourceGroupName    Name       Location          VmSize  OsType            NIC
-----------------    ----       --------          ------  ------            ---
TEST1               test1         eastus Standard_DS1_v2 Windows          test1
TEST1               test2         westus Standard_DS1_v2 Windows          test2
TEST1               test3         eastus Standard_DS1_v2 Windows          test3
TEST2               test4         westus Standard_DS1_v2 Windows          test4
TEST2               test5         eastus Standard_DS1_v2 Windows          test5
```

<span data-ttu-id="25f15-124">Questo comando recupera tutte le macchine virtuali nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="25f15-124">This command gets all the virtual machines in your subscription.</span></span>

### <span data-ttu-id="25f15-125">Esempio 5: Ottenere tutte le macchine virtuali nella posizione.</span><span class="sxs-lookup"><span data-stu-id="25f15-125">Example 5: Get all virtual machines in the location.</span></span>
```
PS C:\> Get-AzVM -Location "westus"

ResourceGroupName    Name       Location          VmSize  OsType            NIC
-----------------    ----       --------          ------  ------            ---
TEST1               test2         westus Standard_DS1_v2 Windows          test2
TEST2               test4         westus Standard_DS1_v2 Windows          test4
```

<span data-ttu-id="25f15-126">Questo comando recupera tutte le macchine virtuali nell'area Degli Stati Uniti occidentali.</span><span class="sxs-lookup"><span data-stu-id="25f15-126">This command gets all the virtual machines in West US region.</span></span>

### <span data-ttu-id="25f15-127">Esempio 6: Usare i filtri per tutte le macchine virtuali</span><span class="sxs-lookup"><span data-stu-id="25f15-127">Example 6: Get all virtual machines using filtering</span></span>
```
PS C:\> Get-AzVM -Name test*

ResourceGroupName    Name       Location          VmSize  OsType            NIC
-----------------    ----       --------          ------  ------            ---
TEST1               test1         eastus Standard_DS1_v2 Windows          test1
TEST1               test2         westus Standard_DS1_v2 Windows          test2
TEST1               test3         eastus Standard_DS1_v2 Windows          test3
TEST2               test4         westus Standard_DS1_v2 Windows          test4
TEST2               test5         eastus Standard_DS1_v2 Windows          test5
```

<span data-ttu-id="25f15-128">Questo comando recupera tutte le macchine virtuali dell'abbonamento che iniziano con "test".</span><span class="sxs-lookup"><span data-stu-id="25f15-128">This command gets all the virtual machines in your subscription that start with "test".</span></span>

## <span data-ttu-id="25f15-129">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25f15-129">PARAMETERS</span></span>

### <span data-ttu-id="25f15-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25f15-130">-DefaultProfile</span></span>
<span data-ttu-id="25f15-131">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="25f15-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25f15-132">-DisplayHint</span><span class="sxs-lookup"><span data-stu-id="25f15-132">-DisplayHint</span></span>
<span data-ttu-id="25f15-133">Determina la modalità di visualizzazione dell'oggetto della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="25f15-133">Determines how the virtual machine object is displayed.</span></span>
<span data-ttu-id="25f15-134">I valori validi sono: -- Compatta: visualizza solo le proprietà di primo livello -- Espandi: visualizza tutte le proprietà in tutti i livelli</span><span class="sxs-lookup"><span data-stu-id="25f15-134">Valid values are: -- Compact: displays only top level properties -- Expand: displays all properties in all levels</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.DisplayHintType
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases:
Accepted values: Compact, Expand

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25f15-135">-Location</span><span class="sxs-lookup"><span data-stu-id="25f15-135">-Location</span></span>
<span data-ttu-id="25f15-136">Specifica una posizione in cui elencare le macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="25f15-136">Specifies a location for the virtual machines to list.</span></span>

```yaml
Type: System.String
Parameter Sets: ListLocationVirtualMachinesParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25f15-137">-Name</span><span class="sxs-lookup"><span data-stu-id="25f15-137">-Name</span></span>
<span data-ttu-id="25f15-138">Specifica il nome della macchina virtuale da ottenere.</span><span class="sxs-lookup"><span data-stu-id="25f15-138">Specifies the name of the virtual machine to get.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParamSet
Aliases: ResourceName, VMName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="25f15-139">-NextLink</span><span class="sxs-lookup"><span data-stu-id="25f15-139">-NextLink</span></span>
<span data-ttu-id="25f15-140">Specifica il collegamento successivo.</span><span class="sxs-lookup"><span data-stu-id="25f15-140">Specifies the next link.</span></span>

```yaml
Type: System.Uri
Parameter Sets: ListNextLinkVirtualMachinesParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25f15-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25f15-141">-ResourceGroupName</span></span>
<span data-ttu-id="25f15-142">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="25f15-142">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParamSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="25f15-143">-Stato</span><span class="sxs-lookup"><span data-stu-id="25f15-143">-Status</span></span>
<span data-ttu-id="25f15-144">Indica che questo cmdlet ottiene solo la visualizzazione dell'istanza della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="25f15-144">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25f15-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25f15-145">CommonParameters</span></span>
<span data-ttu-id="25f15-146">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25f15-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25f15-147">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="25f15-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25f15-148">INPUT</span><span class="sxs-lookup"><span data-stu-id="25f15-148">INPUTS</span></span>

### <span data-ttu-id="25f15-149">System.String</span><span class="sxs-lookup"><span data-stu-id="25f15-149">System.String</span></span>

### <span data-ttu-id="25f15-150">System.Uri</span><span class="sxs-lookup"><span data-stu-id="25f15-150">System.Uri</span></span>

### <span data-ttu-id="25f15-151">Microsoft.Azure.Commands.Compute.Models.DisplayHintType</span><span class="sxs-lookup"><span data-stu-id="25f15-151">Microsoft.Azure.Commands.Compute.Models.DisplayHintType</span></span>

## <span data-ttu-id="25f15-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="25f15-152">OUTPUTS</span></span>

### <span data-ttu-id="25f15-153">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="25f15-153">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="25f15-154">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="25f15-154">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="25f15-155">NOTE</span><span class="sxs-lookup"><span data-stu-id="25f15-155">NOTES</span></span>

## <span data-ttu-id="25f15-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="25f15-156">RELATED LINKS</span></span>

[<span data-ttu-id="25f15-157">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="25f15-157">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="25f15-158">Remove-AZVM</span><span class="sxs-lookup"><span data-stu-id="25f15-158">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="25f15-159">Restart-AZVM</span><span class="sxs-lookup"><span data-stu-id="25f15-159">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="25f15-160">Start-AZVM</span><span class="sxs-lookup"><span data-stu-id="25f15-160">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="25f15-161">Stop-AZVM</span><span class="sxs-lookup"><span data-stu-id="25f15-161">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="25f15-162">Update-AZVM</span><span class="sxs-lookup"><span data-stu-id="25f15-162">Update-AzVM</span></span>](./Update-AzVM.md)


