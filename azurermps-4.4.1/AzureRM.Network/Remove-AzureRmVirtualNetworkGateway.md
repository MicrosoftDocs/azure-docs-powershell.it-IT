---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A35BB728-A7EF-4ADF-B1A9-25A156434E99
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 401fcbd5fca9fc0251e4de0fb7843fb95c1c122d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520485"
---
# <span data-ttu-id="f1988-101">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f1988-101">Remove-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="f1988-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f1988-102">SYNOPSIS</span></span>
<span data-ttu-id="f1988-103">Elimina un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="f1988-103">Deletes a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1988-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f1988-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1988-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1988-105">DESCRIPTION</span></span>
<span data-ttu-id="f1988-106">Il gateway di rete virtuale è l'oggetto che rappresenta il gateway in Azure.</span><span class="sxs-lookup"><span data-stu-id="f1988-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="f1988-107">Il cmdlet **Get-AzureRmVirtualNetworkGateway** restituisce l'oggetto del gateway in Azure in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f1988-107">The **Get-AzureRmVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="f1988-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f1988-108">EXAMPLES</span></span>

### <span data-ttu-id="f1988-109">1: eliminare un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="f1988-109">1: Delete a Virtual Network Gateway</span></span>
```
Remove-AzureRmVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="f1988-110">Elimina l'oggetto del gateway di rete virtuale con il nome "gateway" nel gruppo di risorse "myRG"</span><span class="sxs-lookup"><span data-stu-id="f1988-110">Deletes the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

<span data-ttu-id="f1988-111">Nota: prima di tutto, è necessario eliminare tutte le connessioni al gateway di rete virtuale usando il cmdlet **Remove-AzureRmVirtualNetworkGatewayConnection** .</span><span class="sxs-lookup"><span data-stu-id="f1988-111">Note: You must first delete all connections to the Virtual Network Gateway using the **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="f1988-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f1988-112">PARAMETERS</span></span>

### <span data-ttu-id="f1988-113">-Force</span><span class="sxs-lookup"><span data-stu-id="f1988-113">-Force</span></span>
<span data-ttu-id="f1988-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="f1988-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f1988-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="f1988-115">-Name</span></span>
<span data-ttu-id="f1988-116">Specifica il nome del gateway di rete virtuale rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1988-116">Specifies the name of the virtual network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f1988-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1988-117">-PassThru</span></span>
<span data-ttu-id="f1988-118">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="f1988-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f1988-119">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="f1988-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f1988-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1988-120">-ResourceGroupName</span></span>
<span data-ttu-id="f1988-121">Specifica il nome del gruppo di risorse che contiene il gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="f1988-121">Specifies the name of the resource group that contains the virtual network gateway.</span></span>

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

### <span data-ttu-id="f1988-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f1988-122">-Confirm</span></span>
<span data-ttu-id="f1988-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1988-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1988-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1988-124">-WhatIf</span></span>
<span data-ttu-id="f1988-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f1988-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1988-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f1988-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1988-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1988-127">-DefaultProfile</span></span>
<span data-ttu-id="f1988-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f1988-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1988-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1988-129">CommonParameters</span></span>
<span data-ttu-id="f1988-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1988-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1988-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1988-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1988-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f1988-132">INPUTS</span></span>

## <span data-ttu-id="f1988-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f1988-133">OUTPUTS</span></span>

## <span data-ttu-id="f1988-134">Note</span><span class="sxs-lookup"><span data-stu-id="f1988-134">NOTES</span></span>

## <span data-ttu-id="f1988-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f1988-135">RELATED LINKS</span></span>

