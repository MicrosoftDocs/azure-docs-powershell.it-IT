---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkProfile.md
ms.openlocfilehash: fedf6818f95bd5afadb92c1423a1dbb3296727e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515043"
---
# <span data-ttu-id="ddd08-101">New-AzureRmNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ddd08-101">New-AzureRmNetworkProfile</span></span>

## <span data-ttu-id="ddd08-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ddd08-102">SYNOPSIS</span></span>
<span data-ttu-id="ddd08-103">Crea un nuovo profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="ddd08-103">Creates a new network profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ddd08-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ddd08-104">SYNTAX</span></span>

```
New-AzureRmNetworkProfile -ResourceGroupName <String> -Name <String> [-Location <String>] [-Tag <Hashtable>]
 [-ContainerNicConfig <PSContainerNetworkInterfaceConfiguration[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddd08-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ddd08-105">DESCRIPTION</span></span>
<span data-ttu-id="ddd08-106">Il cmdlet **New-AzureRmNetworkProfile** crea una nuova risorsa di primo livello del profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="ddd08-106">The **New-AzureRmNetworkProfile** cmdlet creates a new network profile top level resource.</span></span>

## <span data-ttu-id="ddd08-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ddd08-107">EXAMPLES</span></span>

### <span data-ttu-id="ddd08-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ddd08-108">Example 1</span></span>
```powershell
$networkProfile = New-AzureRmNetworkProfile -Name np1 -ResourceGroupName rg1 -Location westus
```

<span data-ttu-id="ddd08-109">Verrà creata una nuova risorsa di primo livello del profilo di rete</span><span class="sxs-lookup"><span data-stu-id="ddd08-109">This creates a new network profile top level resource</span></span>

## <span data-ttu-id="ddd08-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ddd08-110">PARAMETERS</span></span>

### <span data-ttu-id="ddd08-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ddd08-111">-AsJob</span></span>
<span data-ttu-id="ddd08-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ddd08-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ddd08-113">-ContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="ddd08-113">-ContainerNicConfig</span></span>
<span data-ttu-id="ddd08-114">Le configurazioni di interfaccia di rete del contenitore da aggiungere al profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="ddd08-114">The container network interface configurations to add to this network profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration[]
Parameter Sets: (All)
Aliases: ContainerNetworkInterfaceConfiguration

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddd08-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddd08-115">-DefaultProfile</span></span>
<span data-ttu-id="ddd08-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ddd08-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddd08-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ddd08-117">-Force</span></span>
<span data-ttu-id="ddd08-118">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="ddd08-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="ddd08-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="ddd08-119">-Location</span></span>
<span data-ttu-id="ddd08-120">La posizione.</span><span class="sxs-lookup"><span data-stu-id="ddd08-120">The location.</span></span>

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

### <span data-ttu-id="ddd08-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="ddd08-121">-Name</span></span>
<span data-ttu-id="ddd08-122">Nome del profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="ddd08-122">The name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddd08-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddd08-123">-ResourceGroupName</span></span>
<span data-ttu-id="ddd08-124">Nome del gruppo di risorse del profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="ddd08-124">The resource group name of the network profile.</span></span>

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

### <span data-ttu-id="ddd08-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="ddd08-125">-Tag</span></span>
<span data-ttu-id="ddd08-126">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="ddd08-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddd08-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ddd08-127">-Confirm</span></span>
<span data-ttu-id="ddd08-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddd08-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd08-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddd08-129">-WhatIf</span></span>
<span data-ttu-id="ddd08-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ddd08-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddd08-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ddd08-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd08-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddd08-132">CommonParameters</span></span>
<span data-ttu-id="ddd08-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddd08-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddd08-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddd08-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddd08-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ddd08-135">INPUTS</span></span>

### <span data-ttu-id="ddd08-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ddd08-136">System.String</span></span>

### <span data-ttu-id="ddd08-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ddd08-137">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ddd08-138">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. Network. Models. PSContainerNetworkInterface, Microsoft. Azure. Commands. Network, Version = 6.7.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ddd08-138">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterface, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="ddd08-139">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. Network. Models. PSContainerNetworkInterfaceConfiguration, Microsoft. Azure. Commands. Network, Version = 6.7.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ddd08-139">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ddd08-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ddd08-140">OUTPUTS</span></span>

### <span data-ttu-id="ddd08-141">Microsoft. Azure. Commands. Network. Models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ddd08-141">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="ddd08-142">Note</span><span class="sxs-lookup"><span data-stu-id="ddd08-142">NOTES</span></span>

## <span data-ttu-id="ddd08-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ddd08-143">RELATED LINKS</span></span>
