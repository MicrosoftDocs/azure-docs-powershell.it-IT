---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A35BB728-A7EF-4ADF-B1A9-25A156434E99
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
ms.openlocfilehash: bb63f9d56dc78943f9232107e39188ae3d29f43f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862918"
---
# <span data-ttu-id="db554-101">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="db554-101">Remove-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="db554-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="db554-102">SYNOPSIS</span></span>
<span data-ttu-id="db554-103">Elimina un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="db554-103">Deletes a Virtual Network Gateway</span></span>

## <span data-ttu-id="db554-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db554-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db554-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db554-105">DESCRIPTION</span></span>
<span data-ttu-id="db554-106">Il gateway di rete virtuale è l'oggetto che rappresenta il gateway in Azure.</span><span class="sxs-lookup"><span data-stu-id="db554-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="db554-107">Il cmdlet **Get-AzVirtualNetworkGateway** restituisce l'oggetto del gateway in Azure in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="db554-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="db554-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db554-108">EXAMPLES</span></span>

### <span data-ttu-id="db554-109">1: eliminare un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="db554-109">1: Delete a Virtual Network Gateway</span></span>
```
Remove-AzVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="db554-110">Elimina l'oggetto del gateway di rete virtuale con il nome "gateway" nel gruppo di risorse "myRG"</span><span class="sxs-lookup"><span data-stu-id="db554-110">Deletes the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

<span data-ttu-id="db554-111">Nota: prima di tutto, è necessario eliminare tutte le connessioni al gateway di rete virtuale usando il cmdlet **Remove-AzVirtualNetworkGatewayConnection** .</span><span class="sxs-lookup"><span data-stu-id="db554-111">Note: You must first delete all connections to the Virtual Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="db554-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="db554-112">PARAMETERS</span></span>

### <span data-ttu-id="db554-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db554-113">-AsJob</span></span>
<span data-ttu-id="db554-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="db554-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="db554-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db554-115">-DefaultProfile</span></span>
<span data-ttu-id="db554-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="db554-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db554-117">-Force</span><span class="sxs-lookup"><span data-stu-id="db554-117">-Force</span></span>
<span data-ttu-id="db554-118">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="db554-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="db554-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="db554-119">-Name</span></span>
<span data-ttu-id="db554-120">Specifica il nome del gateway di rete virtuale rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db554-120">Specifies the name of the virtual network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="db554-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db554-121">-PassThru</span></span>
<span data-ttu-id="db554-122">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="db554-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="db554-123">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="db554-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="db554-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db554-124">-ResourceGroupName</span></span>
<span data-ttu-id="db554-125">Specifica il nome del gruppo di risorse che contiene il gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="db554-125">Specifies the name of the resource group that contains the virtual network gateway.</span></span>

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

### <span data-ttu-id="db554-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="db554-126">-Confirm</span></span>
<span data-ttu-id="db554-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db554-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db554-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db554-128">-WhatIf</span></span>
<span data-ttu-id="db554-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db554-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db554-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db554-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db554-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db554-131">CommonParameters</span></span>
<span data-ttu-id="db554-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db554-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db554-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db554-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db554-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="db554-134">INPUTS</span></span>

## <span data-ttu-id="db554-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db554-135">OUTPUTS</span></span>

## <span data-ttu-id="db554-136">Note</span><span class="sxs-lookup"><span data-stu-id="db554-136">NOTES</span></span>

## <span data-ttu-id="db554-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db554-137">RELATED LINKS</span></span>

