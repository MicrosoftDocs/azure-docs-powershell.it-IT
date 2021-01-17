---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FDA33633-EB2E-4095-8498-DF8910F1D434
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteTable.md
ms.openlocfilehash: 8c899d975669404045aa40bee45ad287a26f8749
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488947"
---
# <span data-ttu-id="a8ec1-101">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="a8ec1-101">Remove-AzRouteTable</span></span>

## <span data-ttu-id="a8ec1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a8ec1-102">SYNOPSIS</span></span>
<span data-ttu-id="a8ec1-103">Rimuove una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="a8ec1-103">Removes a route table.</span></span>

## <span data-ttu-id="a8ec1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a8ec1-104">SYNTAX</span></span>

```
Remove-AzRouteTable -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8ec1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8ec1-105">DESCRIPTION</span></span>
<span data-ttu-id="a8ec1-106">Il cmdlet **Remove-AzRouteTable** rimuove una tabella di route di Azure.</span><span class="sxs-lookup"><span data-stu-id="a8ec1-106">The **Remove-AzRouteTable** cmdlet removes an Azure route table.</span></span>

## <span data-ttu-id="a8ec1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a8ec1-107">EXAMPLES</span></span>

### <span data-ttu-id="a8ec1-108">Esempio 1: rimuovere una tabella di route</span><span class="sxs-lookup"><span data-stu-id="a8ec1-108">Example 1: Remove a route table</span></span>
```
PS C:\>Remove-AzRouteTable -ResourceGroupName "ResourceGroup11 -Name "RouteTable01"
Confirm
Are you sure you want to remove resource 'RouteTable01'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="a8ec1-109">Questo comando consente di rimuovere la tabella di route denominata RouteTable01 nel gruppo di risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="a8ec1-109">This command removes the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>
<span data-ttu-id="a8ec1-110">Il cmdlet richiede conferma prima di rimuovere la tabella.</span><span class="sxs-lookup"><span data-stu-id="a8ec1-110">The cmdlet prompts you for confirmation before it removes the table.</span></span>

## <span data-ttu-id="a8ec1-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a8ec1-111">PARAMETERS</span></span>

### <span data-ttu-id="a8ec1-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a8ec1-112">-AsJob</span></span>
<span data-ttu-id="a8ec1-113">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a8ec1-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a8ec1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8ec1-114">-DefaultProfile</span></span>
<span data-ttu-id="a8ec1-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a8ec1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8ec1-116">-Force</span><span class="sxs-lookup"><span data-stu-id="a8ec1-116">-Force</span></span>
<span data-ttu-id="a8ec1-117">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a8ec1-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a8ec1-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="a8ec1-118">-Name</span></span>
<span data-ttu-id="a8ec1-119">Specifica il nome della tabella di route rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8ec1-119">Specifies the name of the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a8ec1-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8ec1-120">-PassThru</span></span>
<span data-ttu-id="a8ec1-121">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="a8ec1-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a8ec1-122">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="a8ec1-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a8ec1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8ec1-123">-ResourceGroupName</span></span>
<span data-ttu-id="a8ec1-124">Specifica il nome del gruppo di risorse che contiene la tabella di route rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8ec1-124">Specifies the name of the resource group that contains the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a8ec1-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a8ec1-125">-Confirm</span></span>
<span data-ttu-id="a8ec1-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8ec1-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8ec1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8ec1-127">-WhatIf</span></span>
<span data-ttu-id="a8ec1-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a8ec1-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8ec1-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a8ec1-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8ec1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8ec1-130">CommonParameters</span></span>
<span data-ttu-id="a8ec1-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8ec1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8ec1-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8ec1-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8ec1-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a8ec1-133">INPUTS</span></span>

### <span data-ttu-id="a8ec1-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a8ec1-134">System.String</span></span>

## <span data-ttu-id="a8ec1-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a8ec1-135">OUTPUTS</span></span>

### <span data-ttu-id="a8ec1-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a8ec1-136">System.Boolean</span></span>

## <span data-ttu-id="a8ec1-137">Note</span><span class="sxs-lookup"><span data-stu-id="a8ec1-137">NOTES</span></span>

## <span data-ttu-id="a8ec1-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a8ec1-138">RELATED LINKS</span></span>

[<span data-ttu-id="a8ec1-139">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="a8ec1-139">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="a8ec1-140">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="a8ec1-140">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="a8ec1-141">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="a8ec1-141">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


