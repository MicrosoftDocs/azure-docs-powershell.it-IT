---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHub.md
ms.openlocfilehash: 1da7b9981b3c2fe96d895290b7ab73dfc36e183e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515671"
---
# <span data-ttu-id="3e1e0-101">Remove-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="3e1e0-101">Remove-AzureRmIotHub</span></span>

## <span data-ttu-id="3e1e0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3e1e0-102">SYNOPSIS</span></span>
<span data-ttu-id="3e1e0-103">Elimina un IotHub.</span><span class="sxs-lookup"><span data-stu-id="3e1e0-103">Deletes an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e1e0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3e1e0-104">SYNTAX</span></span>

```
Remove-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e1e0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e1e0-105">DESCRIPTION</span></span>
<span data-ttu-id="3e1e0-106">Elimina un IotHub.</span><span class="sxs-lookup"><span data-stu-id="3e1e0-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="3e1e0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3e1e0-107">EXAMPLES</span></span>

### <span data-ttu-id="3e1e0-108">Esempio 1 rimuovere un IotHub</span><span class="sxs-lookup"><span data-stu-id="3e1e0-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="3e1e0-109">Rimuove un IotHub denominato "myiothub"</span><span class="sxs-lookup"><span data-stu-id="3e1e0-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="3e1e0-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3e1e0-110">PARAMETERS</span></span>

### <span data-ttu-id="3e1e0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e1e0-111">-DefaultProfile</span></span>
<span data-ttu-id="3e1e0-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3e1e0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3e1e0-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="3e1e0-113">-Name</span></span>
<span data-ttu-id="3e1e0-114">Nome del IotHub</span><span class="sxs-lookup"><span data-stu-id="3e1e0-114">Name of the IotHub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e1e0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e1e0-115">-ResourceGroupName</span></span>
<span data-ttu-id="3e1e0-116">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="3e1e0-116">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e1e0-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3e1e0-117">-Confirm</span></span>
<span data-ttu-id="3e1e0-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e1e0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e1e0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e1e0-119">-WhatIf</span></span>
<span data-ttu-id="3e1e0-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3e1e0-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e1e0-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3e1e0-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e1e0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e1e0-122">CommonParameters</span></span>
<span data-ttu-id="3e1e0-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e1e0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e1e0-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e1e0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e1e0-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3e1e0-125">INPUTS</span></span>

### <span data-ttu-id="3e1e0-126">System. String</span><span class="sxs-lookup"><span data-stu-id="3e1e0-126">System.String</span></span>

## <span data-ttu-id="3e1e0-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3e1e0-127">OUTPUTS</span></span>

### <span data-ttu-id="3e1e0-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="3e1e0-128">System.Object</span></span>

## <span data-ttu-id="3e1e0-129">Note</span><span class="sxs-lookup"><span data-stu-id="3e1e0-129">NOTES</span></span>

## <span data-ttu-id="3e1e0-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3e1e0-130">RELATED LINKS</span></span>

