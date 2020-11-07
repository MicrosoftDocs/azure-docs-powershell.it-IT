---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: FDA33633-EB2E-4095-8498-DF8910F1D434
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteTable.md
ms.openlocfilehash: ddd1ab1ce748def345604447988d0fc53b5989fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687632"
---
# <span data-ttu-id="e23b9-101">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="e23b9-101">Remove-AzureRmRouteTable</span></span>

## <span data-ttu-id="e23b9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e23b9-102">SYNOPSIS</span></span>
<span data-ttu-id="e23b9-103">Rimuove una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="e23b9-103">Removes a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e23b9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e23b9-104">SYNTAX</span></span>

```
Remove-AzureRmRouteTable -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e23b9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e23b9-105">DESCRIPTION</span></span>
<span data-ttu-id="e23b9-106">Il cmdlet **Remove-AzureRmRouteTable** rimuove una tabella di route di Azure.</span><span class="sxs-lookup"><span data-stu-id="e23b9-106">The **Remove-AzureRmRouteTable** cmdlet removes an Azure route table.</span></span>

## <span data-ttu-id="e23b9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e23b9-107">EXAMPLES</span></span>

### <span data-ttu-id="e23b9-108">Esempio 1: rimuovere una tabella di route</span><span class="sxs-lookup"><span data-stu-id="e23b9-108">Example 1: Remove a route table</span></span>
```
PS C:\>Remove-AzureRmRouteTable -ResourceGroupName "ResourceGroup11 -Name "RouteTable01"
Confirm
Are you sure you want to remove resource 'RouteTable01'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="e23b9-109">Questo comando consente di rimuovere la tabella di route denominata RouteTable01 nel gruppo di risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="e23b9-109">This command removes the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>
<span data-ttu-id="e23b9-110">Il cmdlet richiede conferma prima di rimuovere la tabella.</span><span class="sxs-lookup"><span data-stu-id="e23b9-110">The cmdlet prompts you for confirmation before it removes the table.</span></span>

## <span data-ttu-id="e23b9-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e23b9-111">PARAMETERS</span></span>

### <span data-ttu-id="e23b9-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e23b9-112">-AsJob</span></span>
<span data-ttu-id="e23b9-113">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e23b9-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e23b9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e23b9-114">-DefaultProfile</span></span>
<span data-ttu-id="e23b9-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e23b9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e23b9-116">-Force</span><span class="sxs-lookup"><span data-stu-id="e23b9-116">-Force</span></span>
<span data-ttu-id="e23b9-117">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e23b9-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e23b9-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="e23b9-118">-Name</span></span>
<span data-ttu-id="e23b9-119">Specifica il nome della tabella di route rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e23b9-119">Specifies the name of the route table that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e23b9-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e23b9-120">-PassThru</span></span>
<span data-ttu-id="e23b9-121">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="e23b9-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e23b9-122">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="e23b9-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e23b9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e23b9-123">-ResourceGroupName</span></span>
<span data-ttu-id="e23b9-124">Specifica il nome del gruppo di risorse che contiene la tabella di route rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e23b9-124">Specifies the name of the resource group that contains the route table that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e23b9-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e23b9-125">-Confirm</span></span>
<span data-ttu-id="e23b9-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e23b9-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e23b9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e23b9-127">-WhatIf</span></span>
<span data-ttu-id="e23b9-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e23b9-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e23b9-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e23b9-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e23b9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e23b9-130">CommonParameters</span></span>
<span data-ttu-id="e23b9-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e23b9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e23b9-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e23b9-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e23b9-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e23b9-133">INPUTS</span></span>

### <span data-ttu-id="e23b9-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e23b9-134">None</span></span>
<span data-ttu-id="e23b9-135">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="e23b9-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e23b9-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e23b9-136">OUTPUTS</span></span>

## <span data-ttu-id="e23b9-137">Note</span><span class="sxs-lookup"><span data-stu-id="e23b9-137">NOTES</span></span>

## <span data-ttu-id="e23b9-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e23b9-138">RELATED LINKS</span></span>

[<span data-ttu-id="e23b9-139">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="e23b9-139">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="e23b9-140">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="e23b9-140">New-AzureRmRouteTable</span></span>](./New-AzureRmRouteTable.md)

[<span data-ttu-id="e23b9-141">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="e23b9-141">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)

