---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkTap.md
ms.openlocfilehash: 59e3b7f233077c8ed7064bcb1757634fe08c262b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513608"
---
# <span data-ttu-id="50012-101">Remove-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="50012-101">Remove-AzureRmVirtualNetworkTap</span></span>

## <span data-ttu-id="50012-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="50012-102">SYNOPSIS</span></span>
<span data-ttu-id="50012-103">Consente di rimuovere un tocco di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="50012-103">Removes a virtual network tap.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50012-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="50012-104">SYNTAX</span></span>

### <span data-ttu-id="50012-105">RemoveByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="50012-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzureRmVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50012-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="50012-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzureRmVirtualNetworkTap -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50012-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="50012-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzureRmVirtualNetworkTap -InputObject <PSVirtualNetworkTap> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50012-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50012-108">DESCRIPTION</span></span>
<span data-ttu-id="50012-109">Il cmdlet **Remove-AzureRmVirtualNetworkTap** rimuove un tocco di rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="50012-109">The **Remove-AzureRmVirtualNetworkTap** cmdlet removes an Azure virtual network tap.</span></span>

## <span data-ttu-id="50012-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="50012-110">EXAMPLES</span></span>

### <span data-ttu-id="50012-111">Esempio 1: rimuovere un tocco di rete virtuak</span><span class="sxs-lookup"><span data-stu-id="50012-111">Example 1: Remove a virtuak network tap</span></span>
```
PS C:\>Remove-AzureRmNetworkInterface -Name "VirtualNetworkTap1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="50012-112">Questo comando rimuove il VirtualNetworkTap1 nel gruppo di risorse ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="50012-112">This command removes the VirtualNetworkTap1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="50012-113">Poiché il parametro *Force* non viene usato, all'utente verrà richiesto di confermare questa azione.</span><span class="sxs-lookup"><span data-stu-id="50012-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

## <span data-ttu-id="50012-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="50012-114">PARAMETERS</span></span>

### <span data-ttu-id="50012-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="50012-115">-AsJob</span></span>
<span data-ttu-id="50012-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="50012-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="50012-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50012-117">-DefaultProfile</span></span>
<span data-ttu-id="50012-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="50012-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50012-119">-Force</span><span class="sxs-lookup"><span data-stu-id="50012-119">-Force</span></span>
<span data-ttu-id="50012-120">Non chiedere conferma se si vuole eliminare una risorsa</span><span class="sxs-lookup"><span data-stu-id="50012-120">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="50012-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50012-121">-InputObject</span></span>
<span data-ttu-id="50012-122">Riferimento alla risorsa VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="50012-122">Reference to VirtualNetworkTap resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50012-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="50012-123">-Name</span></span>
<span data-ttu-id="50012-124">Nome del tocco.</span><span class="sxs-lookup"><span data-stu-id="50012-124">The name of the tap.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50012-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="50012-125">-PassThru</span></span>
<span data-ttu-id="50012-126">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="50012-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="50012-127">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="50012-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="50012-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50012-128">-ResourceGroupName</span></span>
<span data-ttu-id="50012-129">Nome del gruppo di risorse del tocco di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="50012-129">The resource group name of the virtual network tap.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50012-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="50012-130">-ResourceId</span></span>
<span data-ttu-id="50012-131">VirtualNetworkTap resourceId</span><span class="sxs-lookup"><span data-stu-id="50012-131">VirtualNetworkTap resourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50012-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="50012-132">-Confirm</span></span>
<span data-ttu-id="50012-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50012-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50012-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50012-134">-WhatIf</span></span>
<span data-ttu-id="50012-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="50012-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50012-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="50012-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50012-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50012-137">CommonParameters</span></span>
<span data-ttu-id="50012-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50012-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50012-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50012-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50012-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="50012-140">INPUTS</span></span>

### <span data-ttu-id="50012-141">System. String</span><span class="sxs-lookup"><span data-stu-id="50012-141">System.String</span></span>

## <span data-ttu-id="50012-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="50012-142">OUTPUTS</span></span>

### <span data-ttu-id="50012-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="50012-143">System.Boolean</span></span>

## <span data-ttu-id="50012-144">Note</span><span class="sxs-lookup"><span data-stu-id="50012-144">NOTES</span></span>

## <span data-ttu-id="50012-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="50012-145">RELATED LINKS</span></span>
