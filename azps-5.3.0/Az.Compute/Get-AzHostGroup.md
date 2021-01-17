---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
ms.openlocfilehash: e0d15be05bf5678eb645a2a26dc2459e6790210a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477832"
---
# <span data-ttu-id="4ab72-101">Get-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="4ab72-101">Get-AzHostGroup</span></span>

## <span data-ttu-id="4ab72-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4ab72-102">SYNOPSIS</span></span>
<span data-ttu-id="4ab72-103">Ottenere o elencare gli host.</span><span class="sxs-lookup"><span data-stu-id="4ab72-103">Get or list hosts.</span></span>

## <span data-ttu-id="4ab72-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4ab72-104">SYNTAX</span></span>

### <span data-ttu-id="4ab72-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4ab72-105">DefaultParameter (Default)</span></span>
```
Get-AzHostGroup [[-ResourceGroupName] <String>] [[-Name] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ab72-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="4ab72-106">ResourceIdParameter</span></span>
```
Get-AzHostGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ab72-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4ab72-107">DESCRIPTION</span></span>
<span data-ttu-id="4ab72-108">Questo cmdlet otterrà un gruppo host.</span><span class="sxs-lookup"><span data-stu-id="4ab72-108">This cmdlet will get a host group.</span></span>
<span data-ttu-id="4ab72-109">Questo cmdlet elenca anche tutti i gruppi host in un gruppo di risorse se non viene assegnato un nome di gruppo host.</span><span class="sxs-lookup"><span data-stu-id="4ab72-109">This cmdlet also lists all host groups in a resource group if a host group name is not given.</span></span>
<span data-ttu-id="4ab72-110">Questo cmdlet elenca anche tutti i gruppi host in una sottoscrizione se non viene assegnato né il nome del gruppo host né il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4ab72-110">This cmdlet also lists all host groups in a subscription if neither host group name nor resource group name is given.</span></span>

## <span data-ttu-id="4ab72-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4ab72-111">EXAMPLES</span></span>

### <span data-ttu-id="4ab72-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4ab72-112">Example 1</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName

ResourceGroupName        : myrg01
PlatformFaultDomainCount : 2
Hosts                    : {/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01}
Zones                    : {1}
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01
Name                     : myhostgroup01
Location                 : eastus
Tags                     : {[key1, val1]}
```

<span data-ttu-id="4ab72-113">Questo comando restituisce un gruppo host.</span><span class="sxs-lookup"><span data-stu-id="4ab72-113">This command returns a host group.</span></span>

### <span data-ttu-id="4ab72-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="4ab72-114">Example 2</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
```

<span data-ttu-id="4ab72-115">Questo comando restituisce tutti i gruppi host nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="4ab72-115">This command returns all host groups in the given resource group.</span></span>

### <span data-ttu-id="4ab72-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="4ab72-116">Example 3</span></span>
```
PS C:\> Get-AzHostGroup

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
myrg02                     myhostgroup03   eastus {[key1, val1]}       2
```

<span data-ttu-id="4ab72-117">Questo comando restituisce tutti i gruppi host nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4ab72-117">This command returns all host groups in the subscription.</span></span>

## <span data-ttu-id="4ab72-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4ab72-118">PARAMETERS</span></span>

### <span data-ttu-id="4ab72-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ab72-119">-DefaultProfile</span></span>
<span data-ttu-id="4ab72-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4ab72-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ab72-121">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="4ab72-121">-InstanceView</span></span>
<span data-ttu-id="4ab72-122">Espandi l'oggetto restituito per elencare anche le visualizzazioni delle istanze dell'host.</span><span class="sxs-lookup"><span data-stu-id="4ab72-122">Expand the returned object to also list the host's instance views.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ab72-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="4ab72-123">-Name</span></span>
<span data-ttu-id="4ab72-124">Nome del gruppo host.</span><span class="sxs-lookup"><span data-stu-id="4ab72-124">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostGroupName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ab72-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ab72-125">-ResourceGroupName</span></span>
<span data-ttu-id="4ab72-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4ab72-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ab72-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ab72-127">-ResourceId</span></span>
<span data-ttu-id="4ab72-128">ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="4ab72-128">The ID of the resource.</span></span>

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

### <span data-ttu-id="4ab72-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ab72-129">CommonParameters</span></span>
<span data-ttu-id="4ab72-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ab72-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ab72-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4ab72-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ab72-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4ab72-132">INPUTS</span></span>

### <span data-ttu-id="4ab72-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4ab72-133">System.String</span></span>

## <span data-ttu-id="4ab72-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4ab72-134">OUTPUTS</span></span>

### <span data-ttu-id="4ab72-135">Microsoft. Azure. Commands. Compute. Automation. Models. PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="4ab72-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="4ab72-136">Note</span><span class="sxs-lookup"><span data-stu-id="4ab72-136">NOTES</span></span>

## <span data-ttu-id="4ab72-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4ab72-137">RELATED LINKS</span></span>
