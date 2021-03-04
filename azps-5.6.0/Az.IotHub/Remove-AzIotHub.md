---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
ms.openlocfilehash: 78478b28e42302ad3a672a0ee889f03807f3d1ae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986032"
---
# <span data-ttu-id="09cc9-101">Remove-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="09cc9-101">Remove-AzIotHub</span></span>

## <span data-ttu-id="09cc9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09cc9-102">SYNOPSIS</span></span>
<span data-ttu-id="09cc9-103">Elimina un iotHub.</span><span class="sxs-lookup"><span data-stu-id="09cc9-103">Deletes an IotHub.</span></span>

## <span data-ttu-id="09cc9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="09cc9-104">SYNTAX</span></span>

```
Remove-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09cc9-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="09cc9-105">DESCRIPTION</span></span>
<span data-ttu-id="09cc9-106">Elimina un iotHub.</span><span class="sxs-lookup"><span data-stu-id="09cc9-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="09cc9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="09cc9-107">EXAMPLES</span></span>

### <span data-ttu-id="09cc9-108">Esempio 1: Rimuovere un iotHub</span><span class="sxs-lookup"><span data-stu-id="09cc9-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="09cc9-109">Rimuove un iotHub denominato "myiothub"</span><span class="sxs-lookup"><span data-stu-id="09cc9-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="09cc9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09cc9-110">PARAMETERS</span></span>

### <span data-ttu-id="09cc9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09cc9-111">-DefaultProfile</span></span>
<span data-ttu-id="09cc9-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="09cc9-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09cc9-113">-Name</span><span class="sxs-lookup"><span data-stu-id="09cc9-113">-Name</span></span>
<span data-ttu-id="09cc9-114">Nome del file IotHub</span><span class="sxs-lookup"><span data-stu-id="09cc9-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="09cc9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09cc9-115">-ResourceGroupName</span></span>
<span data-ttu-id="09cc9-116">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="09cc9-116">Resource Group Name</span></span>

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

### <span data-ttu-id="09cc9-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="09cc9-117">-Confirm</span></span>
<span data-ttu-id="09cc9-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09cc9-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09cc9-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09cc9-119">-WhatIf</span></span>
<span data-ttu-id="09cc9-120">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="09cc9-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09cc9-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="09cc9-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09cc9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09cc9-122">CommonParameters</span></span>
<span data-ttu-id="09cc9-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09cc9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09cc9-124">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09cc9-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09cc9-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="09cc9-125">INPUTS</span></span>

### <span data-ttu-id="09cc9-126">System.String</span><span class="sxs-lookup"><span data-stu-id="09cc9-126">System.String</span></span>

## <span data-ttu-id="09cc9-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="09cc9-127">OUTPUTS</span></span>

### <span data-ttu-id="09cc9-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="09cc9-128">System.Void</span></span>

## <span data-ttu-id="09cc9-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="09cc9-129">NOTES</span></span>

## <span data-ttu-id="09cc9-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="09cc9-130">RELATED LINKS</span></span>
