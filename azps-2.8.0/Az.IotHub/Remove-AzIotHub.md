---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
ms.openlocfilehash: 1529b7b70ec25a7ee8f4b047e28fe77efaf92351
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674208"
---
# <span data-ttu-id="a086d-101">Remove-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="a086d-101">Remove-AzIotHub</span></span>

## <span data-ttu-id="a086d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a086d-102">SYNOPSIS</span></span>
<span data-ttu-id="a086d-103">Elimina un IotHub.</span><span class="sxs-lookup"><span data-stu-id="a086d-103">Deletes an IotHub.</span></span>

## <span data-ttu-id="a086d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a086d-104">SYNTAX</span></span>

```
Remove-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a086d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a086d-105">DESCRIPTION</span></span>
<span data-ttu-id="a086d-106">Elimina un IotHub.</span><span class="sxs-lookup"><span data-stu-id="a086d-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="a086d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a086d-107">EXAMPLES</span></span>

### <span data-ttu-id="a086d-108">Esempio 1 rimuovere un IotHub</span><span class="sxs-lookup"><span data-stu-id="a086d-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="a086d-109">Rimuove un IotHub denominato "myiothub"</span><span class="sxs-lookup"><span data-stu-id="a086d-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="a086d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a086d-110">PARAMETERS</span></span>

### <span data-ttu-id="a086d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a086d-111">-DefaultProfile</span></span>
<span data-ttu-id="a086d-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a086d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a086d-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="a086d-113">-Name</span></span>
<span data-ttu-id="a086d-114">Nome del IotHub</span><span class="sxs-lookup"><span data-stu-id="a086d-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="a086d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a086d-115">-ResourceGroupName</span></span>
<span data-ttu-id="a086d-116">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="a086d-116">Resource Group Name</span></span>

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

### <span data-ttu-id="a086d-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a086d-117">-Confirm</span></span>
<span data-ttu-id="a086d-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a086d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a086d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a086d-119">-WhatIf</span></span>
<span data-ttu-id="a086d-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a086d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a086d-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a086d-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a086d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a086d-122">CommonParameters</span></span>
<span data-ttu-id="a086d-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a086d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a086d-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a086d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a086d-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a086d-125">INPUTS</span></span>

### <span data-ttu-id="a086d-126">System. String</span><span class="sxs-lookup"><span data-stu-id="a086d-126">System.String</span></span>

## <span data-ttu-id="a086d-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a086d-127">OUTPUTS</span></span>

### <span data-ttu-id="a086d-128">System. void</span><span class="sxs-lookup"><span data-stu-id="a086d-128">System.Void</span></span>

## <span data-ttu-id="a086d-129">Note</span><span class="sxs-lookup"><span data-stu-id="a086d-129">NOTES</span></span>

## <span data-ttu-id="a086d-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a086d-130">RELATED LINKS</span></span>