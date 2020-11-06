---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E9390015-FD5C-4015-BA81-3445ADF8F8BF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGateway.md
ms.openlocfilehash: c7ce5872338b9fd3b7741f341d661d09c2eef16a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511684"
---
# <span data-ttu-id="42c1b-101">Remove-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="42c1b-101">Remove-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="42c1b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="42c1b-102">SYNOPSIS</span></span>
<span data-ttu-id="42c1b-103">Rimuove un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="42c1b-103">Removes an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42c1b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="42c1b-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42c1b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="42c1b-105">DESCRIPTION</span></span>
<span data-ttu-id="42c1b-106">Il cmdlet **Remove-AzureRmApplicationGateway** rimuove un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="42c1b-106">The **Remove-AzureRmApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="42c1b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="42c1b-107">EXAMPLES</span></span>

### <span data-ttu-id="42c1b-108">Esempio 1: rimuovere un gateway di applicazione specificato</span><span class="sxs-lookup"><span data-stu-id="42c1b-108">Example 1: Remove a specified application gateway</span></span>
```
PS C:\>Remove-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="42c1b-109">Questo comando rimuove il gateway dell'applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="42c1b-109">This command removes the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="42c1b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="42c1b-110">PARAMETERS</span></span>

### <span data-ttu-id="42c1b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42c1b-111">-DefaultProfile</span></span>
<span data-ttu-id="42c1b-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="42c1b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42c1b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="42c1b-113">-Force</span></span>
<span data-ttu-id="42c1b-114">Indica che il cmdlet impone l'eliminazione del gateway dell'applicazione indipendentemente dal fatto che siano state assegnate risorse.</span><span class="sxs-lookup"><span data-stu-id="42c1b-114">Indicates that the cmdlet forces the deletion of the application gateway regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="42c1b-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="42c1b-115">-Name</span></span>
<span data-ttu-id="42c1b-116">Specifica il nome del gateway dell'applicazione da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="42c1b-116">Specifies the name of the application gateway to be removed.</span></span>

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

### <span data-ttu-id="42c1b-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="42c1b-117">-PassThru</span></span>
<span data-ttu-id="42c1b-118">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="42c1b-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="42c1b-119">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="42c1b-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="42c1b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42c1b-120">-ResourceGroupName</span></span>
<span data-ttu-id="42c1b-121">Specifica il nome del nome del gruppo di risorse a cui appartiene il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="42c1b-121">Specifies the name of the resource group name that the application gateway belongs to.</span></span>

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

### <span data-ttu-id="42c1b-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="42c1b-122">-Confirm</span></span>
<span data-ttu-id="42c1b-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42c1b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42c1b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42c1b-124">-WhatIf</span></span>
<span data-ttu-id="42c1b-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="42c1b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42c1b-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="42c1b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42c1b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42c1b-127">CommonParameters</span></span>
<span data-ttu-id="42c1b-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42c1b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42c1b-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42c1b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42c1b-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="42c1b-130">INPUTS</span></span>

### <span data-ttu-id="42c1b-131">System. String</span><span class="sxs-lookup"><span data-stu-id="42c1b-131">System.String</span></span>

### <span data-ttu-id="42c1b-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="42c1b-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="42c1b-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="42c1b-133">OUTPUTS</span></span>

### <span data-ttu-id="42c1b-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="42c1b-134">System.Boolean</span></span>

## <span data-ttu-id="42c1b-135">Note</span><span class="sxs-lookup"><span data-stu-id="42c1b-135">NOTES</span></span>

## <span data-ttu-id="42c1b-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="42c1b-136">RELATED LINKS</span></span>

[<span data-ttu-id="42c1b-137">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="42c1b-137">Set-AzureRmApplicationGateway</span></span>](./Set-AzureRmApplicationGateway.md)


