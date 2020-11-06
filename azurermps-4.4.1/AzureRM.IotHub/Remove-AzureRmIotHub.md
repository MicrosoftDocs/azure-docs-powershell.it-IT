---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHub.md
ms.openlocfilehash: 0f3a6bfa99a199a737c7a69d151d29f5918cc502
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520074"
---
# <span data-ttu-id="654f1-101">Remove-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="654f1-101">Remove-AzureRmIotHub</span></span>

## <span data-ttu-id="654f1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="654f1-102">SYNOPSIS</span></span>
<span data-ttu-id="654f1-103">Elimina un IotHub.</span><span class="sxs-lookup"><span data-stu-id="654f1-103">Deletes an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="654f1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="654f1-104">SYNTAX</span></span>

```
Remove-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="654f1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="654f1-105">DESCRIPTION</span></span>
<span data-ttu-id="654f1-106">Elimina un IotHub.</span><span class="sxs-lookup"><span data-stu-id="654f1-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="654f1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="654f1-107">EXAMPLES</span></span>

### <span data-ttu-id="654f1-108">Esempio 1 rimuovere un IotHub</span><span class="sxs-lookup"><span data-stu-id="654f1-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="654f1-109">Rimuove un IotHub denominato "myiothub"</span><span class="sxs-lookup"><span data-stu-id="654f1-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="654f1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="654f1-110">PARAMETERS</span></span>

### <span data-ttu-id="654f1-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="654f1-111">-Name</span></span>
<span data-ttu-id="654f1-112">Nome del IotHub</span><span class="sxs-lookup"><span data-stu-id="654f1-112">Name of the IotHub</span></span>

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

### <span data-ttu-id="654f1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="654f1-113">-ResourceGroupName</span></span>
<span data-ttu-id="654f1-114">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="654f1-114">Resource Group Name</span></span>

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

### <span data-ttu-id="654f1-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="654f1-115">-Confirm</span></span>
<span data-ttu-id="654f1-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="654f1-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="654f1-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="654f1-117">-WhatIf</span></span>
<span data-ttu-id="654f1-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="654f1-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="654f1-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="654f1-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="654f1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="654f1-120">-DefaultProfile</span></span>
<span data-ttu-id="654f1-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="654f1-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="654f1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="654f1-122">CommonParameters</span></span>
<span data-ttu-id="654f1-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="654f1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="654f1-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="654f1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="654f1-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="654f1-125">INPUTS</span></span>

### <span data-ttu-id="654f1-126">System. String</span><span class="sxs-lookup"><span data-stu-id="654f1-126">System.String</span></span>

## <span data-ttu-id="654f1-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="654f1-127">OUTPUTS</span></span>

### <span data-ttu-id="654f1-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="654f1-128">System.Object</span></span>

## <span data-ttu-id="654f1-129">Note</span><span class="sxs-lookup"><span data-stu-id="654f1-129">NOTES</span></span>

## <span data-ttu-id="654f1-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="654f1-130">RELATED LINKS</span></span>

