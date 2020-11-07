---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: FDA33633-EB2E-4095-8498-DF8910F1D434
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteTable.md
ms.openlocfilehash: 17cd4ab4e60156c1ab4d6dd4357e638ddaf2c5a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686024"
---
# <span data-ttu-id="c72d0-101">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="c72d0-101">Remove-AzureRmRouteTable</span></span>

## <span data-ttu-id="c72d0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c72d0-102">SYNOPSIS</span></span>
<span data-ttu-id="c72d0-103">Rimuove una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="c72d0-103">Removes a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c72d0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c72d0-104">SYNTAX</span></span>

```
Remove-AzureRmRouteTable -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c72d0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c72d0-105">DESCRIPTION</span></span>
<span data-ttu-id="c72d0-106">Il cmdlet **Remove-AzureRmRouteTable** rimuove una tabella di route di Azure.</span><span class="sxs-lookup"><span data-stu-id="c72d0-106">The **Remove-AzureRmRouteTable** cmdlet removes an Azure route table.</span></span>

## <span data-ttu-id="c72d0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c72d0-107">EXAMPLES</span></span>

### <span data-ttu-id="c72d0-108">Esempio 1: rimuovere una tabella di route</span><span class="sxs-lookup"><span data-stu-id="c72d0-108">Example 1: Remove a route table</span></span>
```
PS C:\>Remove-AzureRmRouteTable -ResourceGroupName "ResourceGroup11 -Name "RouteTable01"
Confirm
Are you sure you want to remove resource 'RouteTable01'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="c72d0-109">Questo comando consente di rimuovere la tabella di route denominata RouteTable01 nel gruppo di risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="c72d0-109">This command removes the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>
<span data-ttu-id="c72d0-110">Il cmdlet richiede conferma prima di rimuovere la tabella.</span><span class="sxs-lookup"><span data-stu-id="c72d0-110">The cmdlet prompts you for confirmation before it removes the table.</span></span>

## <span data-ttu-id="c72d0-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c72d0-111">PARAMETERS</span></span>

### <span data-ttu-id="c72d0-112">-Force</span><span class="sxs-lookup"><span data-stu-id="c72d0-112">-Force</span></span>
<span data-ttu-id="c72d0-113">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c72d0-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c72d0-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="c72d0-114">-Name</span></span>
<span data-ttu-id="c72d0-115">Specifica il nome della tabella di route rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c72d0-115">Specifies the name of the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c72d0-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c72d0-116">-PassThru</span></span>
<span data-ttu-id="c72d0-117">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="c72d0-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c72d0-118">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="c72d0-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c72d0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c72d0-119">-ResourceGroupName</span></span>
<span data-ttu-id="c72d0-120">Specifica il nome del gruppo di risorse che contiene la tabella di route rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c72d0-120">Specifies the name of the resource group that contains the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c72d0-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c72d0-121">-Confirm</span></span>
<span data-ttu-id="c72d0-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c72d0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c72d0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c72d0-123">-WhatIf</span></span>
<span data-ttu-id="c72d0-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c72d0-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c72d0-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c72d0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c72d0-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c72d0-126">-DefaultProfile</span></span>
<span data-ttu-id="c72d0-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c72d0-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c72d0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c72d0-128">CommonParameters</span></span>
<span data-ttu-id="c72d0-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c72d0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c72d0-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c72d0-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c72d0-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c72d0-131">INPUTS</span></span>

## <span data-ttu-id="c72d0-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c72d0-132">OUTPUTS</span></span>

## <span data-ttu-id="c72d0-133">Note</span><span class="sxs-lookup"><span data-stu-id="c72d0-133">NOTES</span></span>

## <span data-ttu-id="c72d0-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c72d0-134">RELATED LINKS</span></span>

[<span data-ttu-id="c72d0-135">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="c72d0-135">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="c72d0-136">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="c72d0-136">New-AzureRmRouteTable</span></span>](./New-AzureRmRouteTable.md)

[<span data-ttu-id="c72d0-137">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="c72d0-137">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)


