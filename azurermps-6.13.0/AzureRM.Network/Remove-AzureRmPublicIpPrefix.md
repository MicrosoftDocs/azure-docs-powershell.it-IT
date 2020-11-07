---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmPublicIpPrefix.md
ms.openlocfilehash: e361e4d3c4daec88ddb35fa7973b65f630dcc390
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687793"
---
# <span data-ttu-id="d23d6-101">Remove-AzureRmPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d23d6-101">Remove-AzureRmPublicIpPrefix</span></span>

## <span data-ttu-id="d23d6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d23d6-102">SYNOPSIS</span></span>
<span data-ttu-id="d23d6-103">Rimuove un prefisso IP pubblico</span><span class="sxs-lookup"><span data-stu-id="d23d6-103">Removes a public IP prefix</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d23d6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d23d6-104">SYNTAX</span></span>

### <span data-ttu-id="d23d6-105">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d23d6-105">RemoveByNameParameterSet</span></span>
```
Remove-AzureRmPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d23d6-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d23d6-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzureRmPublicIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d23d6-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d23d6-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzureRmPublicIpPrefix -InputObject <PSPublicIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d23d6-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d23d6-108">DESCRIPTION</span></span>
<span data-ttu-id="d23d6-109">Il cmdlet \* \* Remove-AzureRmPublicIpPrefix rimuove un prefisso IP pubblico di Azure, purché non siano stati assegnati indirizzi IP pubblici.</span><span class="sxs-lookup"><span data-stu-id="d23d6-109">The \*\*Remove-AzureRmPublicIpPrefix cmdlet removes an Azure public IP prefix as long as there are no public IP addresses allocated from it.</span></span>

## <span data-ttu-id="d23d6-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d23d6-110">EXAMPLES</span></span>

### <span data-ttu-id="d23d6-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d23d6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="d23d6-112">Rimuove il prefisso IP pubblico con il nome $prefixName dal gruppo di risorse $rgName</span><span class="sxs-lookup"><span data-stu-id="d23d6-112">Removes the public IP prefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="d23d6-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d23d6-113">PARAMETERS</span></span>

### <span data-ttu-id="d23d6-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d23d6-114">-AsJob</span></span>
<span data-ttu-id="d23d6-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d23d6-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d23d6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d23d6-116">-DefaultProfile</span></span>
<span data-ttu-id="d23d6-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d23d6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d23d6-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d23d6-118">-Force</span></span>
<span data-ttu-id="d23d6-119">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="d23d6-119">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d23d6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d23d6-120">-InputObject</span></span>
<span data-ttu-id="d23d6-121">Un oggetto PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d23d6-121">A PublicIpPrefix object</span></span>

```yaml
Type: PSPublicIpPrefix
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d23d6-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="d23d6-122">-Name</span></span>
<span data-ttu-id="d23d6-123">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="d23d6-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d23d6-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d23d6-124">-PassThru</span></span>
<span data-ttu-id="d23d6-125">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="d23d6-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d23d6-126">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="d23d6-126">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d23d6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d23d6-127">-ResourceGroupName</span></span>
<span data-ttu-id="d23d6-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d23d6-128">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d23d6-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d23d6-129">-ResourceId</span></span>
<span data-ttu-id="d23d6-130">ResourceId per la risorsa da rimuovere</span><span class="sxs-lookup"><span data-stu-id="d23d6-130">The resourceId for the resource to remove</span></span>

```yaml
Type: String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d23d6-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d23d6-131">-Confirm</span></span>
<span data-ttu-id="d23d6-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d23d6-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d23d6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d23d6-133">-WhatIf</span></span>
<span data-ttu-id="d23d6-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d23d6-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d23d6-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d23d6-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d23d6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d23d6-136">CommonParameters</span></span>
<span data-ttu-id="d23d6-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d23d6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d23d6-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d23d6-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d23d6-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d23d6-139">INPUTS</span></span>

### <span data-ttu-id="d23d6-140">System. String</span><span class="sxs-lookup"><span data-stu-id="d23d6-140">System.String</span></span>
<span data-ttu-id="d23d6-141">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d23d6-141">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>


## <span data-ttu-id="d23d6-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d23d6-142">OUTPUTS</span></span>

### <span data-ttu-id="d23d6-143">System. Object</span><span class="sxs-lookup"><span data-stu-id="d23d6-143">System.Object</span></span>

## <span data-ttu-id="d23d6-144">Note</span><span class="sxs-lookup"><span data-stu-id="d23d6-144">NOTES</span></span>

## <span data-ttu-id="d23d6-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d23d6-145">RELATED LINKS</span></span>
