---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHost.md
ms.openlocfilehash: cc9b536517a70fd7c004be6fcac300afa0a4760b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675431"
---
# <span data-ttu-id="51794-101">Get-AzHost</span><span class="sxs-lookup"><span data-stu-id="51794-101">Get-AzHost</span></span>

## <span data-ttu-id="51794-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="51794-102">SYNOPSIS</span></span>
<span data-ttu-id="51794-103">Ottenere o elencare gli host.</span><span class="sxs-lookup"><span data-stu-id="51794-103">Get or list hosts.</span></span>

## <span data-ttu-id="51794-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="51794-104">SYNTAX</span></span>

### <span data-ttu-id="51794-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="51794-105">DefaultParameter (Default)</span></span>
```
Get-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [[-Name] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51794-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="51794-106">ResourceIdParameter</span></span>
```
Get-AzHost [-ResourceId] <String> [-InstanceView] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="51794-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="51794-107">DESCRIPTION</span></span>
<span data-ttu-id="51794-108">Questo cmdlet otterrà un host in un gruppo host.</span><span class="sxs-lookup"><span data-stu-id="51794-108">This cmdlet will get a host in a host group.</span></span>
<span data-ttu-id="51794-109">Questo cmdlet elenca anche tutti gli host di un gruppo host se non viene assegnato un nome host.</span><span class="sxs-lookup"><span data-stu-id="51794-109">This cmdlet also lists all hosts in a host group if a host name is not given.</span></span>

## <span data-ttu-id="51794-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="51794-110">EXAMPLES</span></span>

### <span data-ttu-id="51794-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="51794-111">Example 1</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName

ResourceGroupName    : myrg01
PlatformFaultDomain  : 1
AutoReplaceOnFailure : True
HostId               : 00000000-0000-0000-0000-000000000000
VirtualMachines[0]   : 
  Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/virtualMachines/myvm01
VirtualMachines[1]   : 
  Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/virtualMachines/myvm02
ProvisioningTime     : 7/27/2019 3:22:59 AM
ProvisioningState    : Succeeded
Sku                  : 
  Name               : ESv3-Type1
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01
Name                 : myhost01
Location             : eastus
Tags                 : {"key1":"val2"}
```

<span data-ttu-id="51794-112">Questo comando restituisce un host.</span><span class="sxs-lookup"><span data-stu-id="51794-112">This command returns a host.</span></span>

### <span data-ttu-id="51794-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="51794-113">Example 2</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName -InstanceView

ResourceGroupName      : myrg01
PlatformFaultDomain    : 0
AutoReplaceOnFailure   : True
HostId                 : 00000000-0000-0000-0000-000000000000
ProvisioningTime       : 8/19/2019 9:13:19 PM
ProvisioningState      : Succeeded
InstanceView           : 
  AssetId              : 00000000-0000-0000-0000-000000000000
  AvailableCapacity    : 
    AllocatableVMs[0]  : 
      VmSize           : Standard_E2s_v3
      Count            : 28
    AllocatableVMs[1]  : 
      VmSize           : Standard_E4-2s_v3
      Count            : 14
    AllocatableVMs[2]  : 
      VmSize           : Standard_E4s_v3
      Count            : 14
  Statuses[0]          : 
    Code               : ProvisioningState/succeeded
    Level              : Info
    DisplayStatus      : Provisioning succeeded
    Time               : 8/19/2019 9:13:19 PM
  Statuses[1]          : 
    Code               : HealthState/available
    Level              : Info
    DisplayStatus      : Host available
Sku                    : 
  Name                 : ESv3-Type1
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01
Name                   : crptestps2264host
Location               : eastus
Tags                   : {"key1":"val2"}
```

<span data-ttu-id="51794-114">Questo comando restituisce la visualizzazione dell'istanza di un host.</span><span class="sxs-lookup"><span data-stu-id="51794-114">This command returns the instance view of a host.</span></span>

### <span data-ttu-id="51794-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="51794-115">Example 3</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName

ResourceGroupName       Name Location           Tags        Sku FD
-----------------       ---- --------           ----        --- --
myrg01              myhost01   eastus {[key1, val2]} ESv3-Type1  0
myrg01              myhost02   eastus {[key1, val2]} ESv3-Type1  1
```

<span data-ttu-id="51794-116">Questo comando restituisce tutti gli host nel gruppo host specificato.</span><span class="sxs-lookup"><span data-stu-id="51794-116">This command returns all hosts in the given host group.</span></span>

## <span data-ttu-id="51794-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="51794-117">PARAMETERS</span></span>

### <span data-ttu-id="51794-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51794-118">-DefaultProfile</span></span>
<span data-ttu-id="51794-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="51794-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51794-120">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="51794-120">-HostGroupName</span></span>
<span data-ttu-id="51794-121">Nome del gruppo host.</span><span class="sxs-lookup"><span data-stu-id="51794-121">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51794-122">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="51794-122">-InstanceView</span></span>
<span data-ttu-id="51794-123">Indica che questo cmdlet ottiene solo la visualizzazione dell'istanza dell'host.</span><span class="sxs-lookup"><span data-stu-id="51794-123">Indicates that this cmdlet gets only the instance view of the host.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51794-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="51794-124">-Name</span></span>
<span data-ttu-id="51794-125">Nome dell'host.</span><span class="sxs-lookup"><span data-stu-id="51794-125">The name of the host.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51794-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51794-126">-ResourceGroupName</span></span>
<span data-ttu-id="51794-127">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="51794-127">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51794-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51794-128">-ResourceId</span></span>
<span data-ttu-id="51794-129">ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="51794-129">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51794-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51794-130">CommonParameters</span></span>
<span data-ttu-id="51794-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51794-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51794-132">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="51794-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51794-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="51794-133">INPUTS</span></span>

### <span data-ttu-id="51794-134">System. String</span><span class="sxs-lookup"><span data-stu-id="51794-134">System.String</span></span>

## <span data-ttu-id="51794-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="51794-135">OUTPUTS</span></span>

### <span data-ttu-id="51794-136">Microsoft. Azure. Commands. Compute. Automation. Models. PSHost</span><span class="sxs-lookup"><span data-stu-id="51794-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="51794-137">Note</span><span class="sxs-lookup"><span data-stu-id="51794-137">NOTES</span></span>

## <span data-ttu-id="51794-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="51794-138">RELATED LINKS</span></span>
