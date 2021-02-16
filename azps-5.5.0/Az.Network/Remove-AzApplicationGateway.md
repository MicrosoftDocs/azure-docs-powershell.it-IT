---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E9390015-FD5C-4015-BA81-3445ADF8F8BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGateway.md
ms.openlocfilehash: aa8c40d7fb9f5ccb99ccdd88d6c04ceb4a888bf2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191799"
---
# <span data-ttu-id="c4227-101">Remove-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c4227-101">Remove-AzApplicationGateway</span></span>

## <span data-ttu-id="c4227-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4227-102">SYNOPSIS</span></span>
<span data-ttu-id="c4227-103">Rimuove un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="c4227-103">Removes an application gateway.</span></span>

## <span data-ttu-id="c4227-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c4227-104">SYNTAX</span></span>

```
Remove-AzApplicationGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4227-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c4227-105">DESCRIPTION</span></span>
<span data-ttu-id="c4227-106">Il cmdlet **Remove-AzApplicationGateway** rimuove un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="c4227-106">The **Remove-AzApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="c4227-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c4227-107">EXAMPLES</span></span>

### <span data-ttu-id="c4227-108">Esempio 1: Rimuovere un gateway applicazione specificato</span><span class="sxs-lookup"><span data-stu-id="c4227-108">Example 1: Remove a specified application gateway</span></span>
```
PS C:\>Remove-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="c4227-109">Questo comando rimuove il gateway applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="c4227-109">This command removes the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="c4227-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4227-110">PARAMETERS</span></span>

### <span data-ttu-id="c4227-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4227-111">-DefaultProfile</span></span>
<span data-ttu-id="c4227-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c4227-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4227-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c4227-113">-Force</span></span>
<span data-ttu-id="c4227-114">Indica che il cmdlet forza l'eliminazione del gateway applicazione indipendentemente dal fatto che le risorse siano assegnate o meno.</span><span class="sxs-lookup"><span data-stu-id="c4227-114">Indicates that the cmdlet forces the deletion of the application gateway regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="c4227-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c4227-115">-Name</span></span>
<span data-ttu-id="c4227-116">Specifica il nome del gateway applicazione da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="c4227-116">Specifies the name of the application gateway to be removed.</span></span>

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

### <span data-ttu-id="c4227-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4227-117">-PassThru</span></span>
<span data-ttu-id="c4227-118">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="c4227-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c4227-119">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="c4227-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c4227-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4227-120">-ResourceGroupName</span></span>
<span data-ttu-id="c4227-121">Specifica il nome del gruppo di risorse a cui appartiene il gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="c4227-121">Specifies the name of the resource group name that the application gateway belongs to.</span></span>

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

### <span data-ttu-id="c4227-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c4227-122">-Confirm</span></span>
<span data-ttu-id="c4227-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4227-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4227-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4227-124">-WhatIf</span></span>
<span data-ttu-id="c4227-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c4227-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4227-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c4227-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4227-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4227-127">CommonParameters</span></span>
<span data-ttu-id="c4227-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4227-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4227-129">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4227-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4227-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="c4227-130">INPUTS</span></span>

### <span data-ttu-id="c4227-131">System.String</span><span class="sxs-lookup"><span data-stu-id="c4227-131">System.String</span></span>

### <span data-ttu-id="c4227-132">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c4227-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c4227-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c4227-133">OUTPUTS</span></span>

### <span data-ttu-id="c4227-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c4227-134">System.Boolean</span></span>

## <span data-ttu-id="c4227-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="c4227-135">NOTES</span></span>

## <span data-ttu-id="c4227-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c4227-136">RELATED LINKS</span></span>

[<span data-ttu-id="c4227-137">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c4227-137">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)


