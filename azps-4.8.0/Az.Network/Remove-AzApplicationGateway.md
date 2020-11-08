---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E9390015-FD5C-4015-BA81-3445ADF8F8BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGateway.md
ms.openlocfilehash: aa8c40d7fb9f5ccb99ccdd88d6c04ceb4a888bf2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192308"
---
# <span data-ttu-id="b95cc-101">Remove-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b95cc-101">Remove-AzApplicationGateway</span></span>

## <span data-ttu-id="b95cc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b95cc-102">SYNOPSIS</span></span>
<span data-ttu-id="b95cc-103">Rimuove un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b95cc-103">Removes an application gateway.</span></span>

## <span data-ttu-id="b95cc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b95cc-104">SYNTAX</span></span>

```
Remove-AzApplicationGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b95cc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b95cc-105">DESCRIPTION</span></span>
<span data-ttu-id="b95cc-106">Il cmdlet **Remove-AzApplicationGateway** rimuove un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b95cc-106">The **Remove-AzApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="b95cc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b95cc-107">EXAMPLES</span></span>

### <span data-ttu-id="b95cc-108">Esempio 1: rimuovere un gateway di applicazione specificato</span><span class="sxs-lookup"><span data-stu-id="b95cc-108">Example 1: Remove a specified application gateway</span></span>
```
PS C:\>Remove-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="b95cc-109">Questo comando rimuove il gateway dell'applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="b95cc-109">This command removes the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="b95cc-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b95cc-110">PARAMETERS</span></span>

### <span data-ttu-id="b95cc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b95cc-111">-DefaultProfile</span></span>
<span data-ttu-id="b95cc-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b95cc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b95cc-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b95cc-113">-Force</span></span>
<span data-ttu-id="b95cc-114">Indica che il cmdlet impone l'eliminazione del gateway dell'applicazione indipendentemente dal fatto che siano state assegnate risorse.</span><span class="sxs-lookup"><span data-stu-id="b95cc-114">Indicates that the cmdlet forces the deletion of the application gateway regardless of whether resources are assigned to it.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b95cc-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="b95cc-115">-Name</span></span>
<span data-ttu-id="b95cc-116">Specifica il nome del gateway dell'applicazione da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="b95cc-116">Specifies the name of the application gateway to be removed.</span></span>

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

### <span data-ttu-id="b95cc-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b95cc-117">-PassThru</span></span>
<span data-ttu-id="b95cc-118">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="b95cc-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b95cc-119">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="b95cc-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b95cc-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b95cc-120">-ResourceGroupName</span></span>
<span data-ttu-id="b95cc-121">Specifica il nome del nome del gruppo di risorse a cui appartiene il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b95cc-121">Specifies the name of the resource group name that the application gateway belongs to.</span></span>

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

### <span data-ttu-id="b95cc-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b95cc-122">-Confirm</span></span>
<span data-ttu-id="b95cc-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b95cc-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b95cc-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b95cc-124">-WhatIf</span></span>
<span data-ttu-id="b95cc-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b95cc-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b95cc-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b95cc-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b95cc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b95cc-127">CommonParameters</span></span>
<span data-ttu-id="b95cc-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b95cc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b95cc-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b95cc-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b95cc-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b95cc-130">INPUTS</span></span>

### <span data-ttu-id="b95cc-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b95cc-131">System.String</span></span>

### <span data-ttu-id="b95cc-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b95cc-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b95cc-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b95cc-133">OUTPUTS</span></span>

### <span data-ttu-id="b95cc-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b95cc-134">System.Boolean</span></span>

## <span data-ttu-id="b95cc-135">Note</span><span class="sxs-lookup"><span data-stu-id="b95cc-135">NOTES</span></span>

## <span data-ttu-id="b95cc-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b95cc-136">RELATED LINKS</span></span>

[<span data-ttu-id="b95cc-137">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b95cc-137">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)

