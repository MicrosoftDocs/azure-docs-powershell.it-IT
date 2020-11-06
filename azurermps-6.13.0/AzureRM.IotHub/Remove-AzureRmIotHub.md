---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHub.md
ms.openlocfilehash: 674105b31c06d3def687bfc58f8b16be1c6b86f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515224"
---
# <span data-ttu-id="cdc70-101">Remove-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="cdc70-101">Remove-AzureRmIotHub</span></span>

## <span data-ttu-id="cdc70-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cdc70-102">SYNOPSIS</span></span>
<span data-ttu-id="cdc70-103">Elimina un IotHub.</span><span class="sxs-lookup"><span data-stu-id="cdc70-103">Deletes an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cdc70-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cdc70-104">SYNTAX</span></span>

```
Remove-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdc70-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cdc70-105">DESCRIPTION</span></span>
<span data-ttu-id="cdc70-106">Elimina un IotHub.</span><span class="sxs-lookup"><span data-stu-id="cdc70-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="cdc70-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cdc70-107">EXAMPLES</span></span>

### <span data-ttu-id="cdc70-108">Esempio 1 rimuovere un IotHub</span><span class="sxs-lookup"><span data-stu-id="cdc70-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="cdc70-109">Rimuove un IotHub denominato "myiothub"</span><span class="sxs-lookup"><span data-stu-id="cdc70-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="cdc70-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cdc70-110">PARAMETERS</span></span>

### <span data-ttu-id="cdc70-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdc70-111">-DefaultProfile</span></span>
<span data-ttu-id="cdc70-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="cdc70-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cdc70-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="cdc70-113">-Name</span></span>
<span data-ttu-id="cdc70-114">Nome del IotHub</span><span class="sxs-lookup"><span data-stu-id="cdc70-114">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdc70-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdc70-115">-ResourceGroupName</span></span>
<span data-ttu-id="cdc70-116">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="cdc70-116">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdc70-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cdc70-117">-Confirm</span></span>
<span data-ttu-id="cdc70-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdc70-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdc70-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdc70-119">-WhatIf</span></span>
<span data-ttu-id="cdc70-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cdc70-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdc70-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cdc70-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdc70-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdc70-122">CommonParameters</span></span>
<span data-ttu-id="cdc70-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdc70-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdc70-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdc70-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdc70-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cdc70-125">INPUTS</span></span>

### <span data-ttu-id="cdc70-126">System. String</span><span class="sxs-lookup"><span data-stu-id="cdc70-126">System.String</span></span>

## <span data-ttu-id="cdc70-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cdc70-127">OUTPUTS</span></span>

### <span data-ttu-id="cdc70-128">System. void</span><span class="sxs-lookup"><span data-stu-id="cdc70-128">System.Void</span></span>

## <span data-ttu-id="cdc70-129">Note</span><span class="sxs-lookup"><span data-stu-id="cdc70-129">NOTES</span></span>

## <span data-ttu-id="cdc70-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cdc70-130">RELATED LINKS</span></span>
