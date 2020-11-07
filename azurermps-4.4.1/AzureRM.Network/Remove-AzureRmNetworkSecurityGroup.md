---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 01F56553-1685-43D4-89E6-DDCDF17D1E00
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: fd6d9a09bd2c4fa597d2c384d3ba8e730b3f1102
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686025"
---
# <span data-ttu-id="d6629-101">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d6629-101">Remove-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="d6629-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d6629-102">SYNOPSIS</span></span>
<span data-ttu-id="d6629-103">Rimuove un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="d6629-103">Removes a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6629-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d6629-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6629-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d6629-105">DESCRIPTION</span></span>
<span data-ttu-id="d6629-106">Il cmdlet **Remove-AzureRmNetworkSecurityGroup** rimuove un gruppo di sicurezza di rete Azure.</span><span class="sxs-lookup"><span data-stu-id="d6629-106">The **Remove-AzureRmNetworkSecurityGroup** cmdlet removes an Azure network security group.</span></span>

## <span data-ttu-id="d6629-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d6629-107">EXAMPLES</span></span>

### <span data-ttu-id="d6629-108">Esempio 1: rimuovere un gruppo di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="d6629-108">Example 1: Remove a network security group</span></span>
```
PS C:\>Remove-AzureRmNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
```

<span data-ttu-id="d6629-109">Questo comando rimuove il gruppo di sicurezza denominato NSG-FrontEnd nel gruppo di risorse denominato TestRG.</span><span class="sxs-lookup"><span data-stu-id="d6629-109">This command removes the security group named NSG-FrontEnd in the resource group named TestRG.</span></span>

## <span data-ttu-id="d6629-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d6629-110">PARAMETERS</span></span>

### <span data-ttu-id="d6629-111">-Force</span><span class="sxs-lookup"><span data-stu-id="d6629-111">-Force</span></span>
<span data-ttu-id="d6629-112">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d6629-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d6629-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="d6629-113">-Name</span></span>
<span data-ttu-id="d6629-114">Specifica il nome del gruppo di sicurezza di rete rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6629-114">Specifies the name of the network security group that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d6629-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d6629-115">-PassThru</span></span>
<span data-ttu-id="d6629-116">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="d6629-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d6629-117">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="d6629-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d6629-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6629-118">-ResourceGroupName</span></span>
<span data-ttu-id="d6629-119">Specifica il nome di un gruppo di risorse da cui questo cmdlet rimuove un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="d6629-119">Specifies the name of a resource group that this cmdlet removes a network security group from.</span></span>

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

### <span data-ttu-id="d6629-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d6629-120">-Confirm</span></span>
<span data-ttu-id="d6629-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6629-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6629-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6629-122">-WhatIf</span></span>
<span data-ttu-id="d6629-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d6629-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6629-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d6629-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6629-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6629-125">-DefaultProfile</span></span>
<span data-ttu-id="d6629-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d6629-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6629-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6629-127">CommonParameters</span></span>
<span data-ttu-id="d6629-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6629-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6629-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6629-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6629-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d6629-130">INPUTS</span></span>

## <span data-ttu-id="d6629-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d6629-131">OUTPUTS</span></span>

## <span data-ttu-id="d6629-132">Note</span><span class="sxs-lookup"><span data-stu-id="d6629-132">NOTES</span></span>

## <span data-ttu-id="d6629-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d6629-133">RELATED LINKS</span></span>

[<span data-ttu-id="d6629-134">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d6629-134">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="d6629-135">New-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d6629-135">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="d6629-136">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d6629-136">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)


