---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E9390015-FD5C-4015-BA81-3445ADF8F8BF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGateway.md
ms.openlocfilehash: b743c9b2fa0e8abff1a878b6cdb780c025300ba7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509808"
---
# <span data-ttu-id="780cc-101">Remove-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="780cc-101">Remove-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="780cc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="780cc-102">SYNOPSIS</span></span>
<span data-ttu-id="780cc-103">Rimuove un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="780cc-103">Removes an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="780cc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="780cc-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="780cc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="780cc-105">DESCRIPTION</span></span>
<span data-ttu-id="780cc-106">Il cmdlet **Remove-AzureRmApplicationGateway** rimuove un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="780cc-106">The **Remove-AzureRmApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="780cc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="780cc-107">EXAMPLES</span></span>

### <span data-ttu-id="780cc-108">Esempio 1: rimuovere un gateway di applicazione specificato</span><span class="sxs-lookup"><span data-stu-id="780cc-108">Example 1: Remove a specified application gateway</span></span>
```
PS C:\>Remove-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="780cc-109">Questo comando rimuove il gateway dell'applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="780cc-109">This command removes the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="780cc-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="780cc-110">PARAMETERS</span></span>

### <span data-ttu-id="780cc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="780cc-111">-DefaultProfile</span></span>
<span data-ttu-id="780cc-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="780cc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="780cc-113">-Force</span><span class="sxs-lookup"><span data-stu-id="780cc-113">-Force</span></span>
<span data-ttu-id="780cc-114">Indica che il cmdlet impone l'eliminazione del gateway dell'applicazione indipendentemente dal fatto che siano state assegnate risorse.</span><span class="sxs-lookup"><span data-stu-id="780cc-114">Indicates that the cmdlet forces the deletion of the application gateway regardless of whether resources are assigned to it.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="780cc-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="780cc-115">-Name</span></span>
<span data-ttu-id="780cc-116">Specifica il nome del gateway dell'applicazione da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="780cc-116">Specifies the name of the application gateway to be removed.</span></span>

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

### <span data-ttu-id="780cc-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="780cc-117">-PassThru</span></span>
<span data-ttu-id="780cc-118">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="780cc-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="780cc-119">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="780cc-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="780cc-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="780cc-120">-ResourceGroupName</span></span>
<span data-ttu-id="780cc-121">Specifica il nome del nome del gruppo di risorse a cui appartiene il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="780cc-121">Specifies the name of the resource group name that the application gateway belongs to.</span></span>

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

### <span data-ttu-id="780cc-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="780cc-122">-Confirm</span></span>
<span data-ttu-id="780cc-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="780cc-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="780cc-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="780cc-124">-WhatIf</span></span>
<span data-ttu-id="780cc-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="780cc-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="780cc-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="780cc-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="780cc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="780cc-127">CommonParameters</span></span>
<span data-ttu-id="780cc-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="780cc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="780cc-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="780cc-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="780cc-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="780cc-130">INPUTS</span></span>

### <span data-ttu-id="780cc-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="780cc-131">None</span></span>
<span data-ttu-id="780cc-132">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="780cc-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="780cc-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="780cc-133">OUTPUTS</span></span>

### <span data-ttu-id="780cc-134">System. String</span><span class="sxs-lookup"><span data-stu-id="780cc-134">System.String</span></span>

## <span data-ttu-id="780cc-135">Note</span><span class="sxs-lookup"><span data-stu-id="780cc-135">NOTES</span></span>

## <span data-ttu-id="780cc-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="780cc-136">RELATED LINKS</span></span>

[<span data-ttu-id="780cc-137">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="780cc-137">Set-AzureRmApplicationGateway</span></span>](./Set-AzureRmApplicationGateway.md)


