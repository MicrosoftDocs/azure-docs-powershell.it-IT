---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 01F56553-1685-43D4-89E6-DDCDF17D1E00
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworksecuritygroup
schema: 2.0.0
ms.openlocfilehash: 32709a1a0280604b784c9f094478858f8c4bc4ab
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866048"
---
# <span data-ttu-id="981a7-101">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="981a7-101">Remove-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="981a7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="981a7-102">SYNOPSIS</span></span>
<span data-ttu-id="981a7-103">Rimuove un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="981a7-103">Removes a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="981a7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="981a7-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="981a7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="981a7-105">DESCRIPTION</span></span>
<span data-ttu-id="981a7-106">Il cmdlet **Remove-AzureRmNetworkSecurityGroup** rimuove un gruppo di sicurezza di rete Azure.</span><span class="sxs-lookup"><span data-stu-id="981a7-106">The **Remove-AzureRmNetworkSecurityGroup** cmdlet removes an Azure network security group.</span></span>

## <span data-ttu-id="981a7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="981a7-107">EXAMPLES</span></span>

### <span data-ttu-id="981a7-108">Esempio 1: rimuovere un gruppo di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="981a7-108">Example 1: Remove a network security group</span></span>
```
PS C:\>Remove-AzureRmNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
```

<span data-ttu-id="981a7-109">Questo comando rimuove il gruppo di sicurezza denominato NSG-FrontEnd nel gruppo di risorse denominato TestRG.</span><span class="sxs-lookup"><span data-stu-id="981a7-109">This command removes the security group named NSG-FrontEnd in the resource group named TestRG.</span></span>

## <span data-ttu-id="981a7-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="981a7-110">PARAMETERS</span></span>

### <span data-ttu-id="981a7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="981a7-111">-AsJob</span></span>
<span data-ttu-id="981a7-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="981a7-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="981a7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="981a7-113">-DefaultProfile</span></span>
<span data-ttu-id="981a7-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="981a7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="981a7-115">-Force</span><span class="sxs-lookup"><span data-stu-id="981a7-115">-Force</span></span>
<span data-ttu-id="981a7-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="981a7-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="981a7-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="981a7-117">-Name</span></span>
<span data-ttu-id="981a7-118">Specifica il nome del gruppo di sicurezza di rete rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="981a7-118">Specifies the name of the network security group that this cmdlet removes.</span></span>

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

### <span data-ttu-id="981a7-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="981a7-119">-PassThru</span></span>
<span data-ttu-id="981a7-120">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="981a7-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="981a7-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="981a7-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="981a7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="981a7-122">-ResourceGroupName</span></span>
<span data-ttu-id="981a7-123">Specifica il nome di un gruppo di risorse da cui questo cmdlet rimuove un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="981a7-123">Specifies the name of a resource group that this cmdlet removes a network security group from.</span></span>

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

### <span data-ttu-id="981a7-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="981a7-124">-Confirm</span></span>
<span data-ttu-id="981a7-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="981a7-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="981a7-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="981a7-126">-WhatIf</span></span>
<span data-ttu-id="981a7-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="981a7-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="981a7-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="981a7-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="981a7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="981a7-129">CommonParameters</span></span>
<span data-ttu-id="981a7-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="981a7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="981a7-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="981a7-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="981a7-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="981a7-132">INPUTS</span></span>

## <span data-ttu-id="981a7-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="981a7-133">OUTPUTS</span></span>

## <span data-ttu-id="981a7-134">Note</span><span class="sxs-lookup"><span data-stu-id="981a7-134">NOTES</span></span>

## <span data-ttu-id="981a7-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="981a7-135">RELATED LINKS</span></span>

[<span data-ttu-id="981a7-136">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="981a7-136">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="981a7-137">New-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="981a7-137">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="981a7-138">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="981a7-138">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)


