---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
ms.openlocfilehash: 4e851c6a65e2ff69e6675a2e057a1ed319ba6519
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200087"
---
# <span data-ttu-id="84af1-101">Remove-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="84af1-101">Remove-AzIotHub</span></span>

## <span data-ttu-id="84af1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84af1-102">SYNOPSIS</span></span>
<span data-ttu-id="84af1-103">Elimina un iotHub.</span><span class="sxs-lookup"><span data-stu-id="84af1-103">Deletes an IotHub.</span></span>

## <span data-ttu-id="84af1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="84af1-104">SYNTAX</span></span>

```
Remove-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84af1-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="84af1-105">DESCRIPTION</span></span>
<span data-ttu-id="84af1-106">Elimina un iotHub.</span><span class="sxs-lookup"><span data-stu-id="84af1-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="84af1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="84af1-107">EXAMPLES</span></span>

### <span data-ttu-id="84af1-108">Esempio 1: Rimuovere un iotHub</span><span class="sxs-lookup"><span data-stu-id="84af1-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="84af1-109">Rimuove un IotHub denominato "myiothub"</span><span class="sxs-lookup"><span data-stu-id="84af1-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="84af1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84af1-110">PARAMETERS</span></span>

### <span data-ttu-id="84af1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84af1-111">-DefaultProfile</span></span>
<span data-ttu-id="84af1-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="84af1-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="84af1-113">-Name</span><span class="sxs-lookup"><span data-stu-id="84af1-113">-Name</span></span>
<span data-ttu-id="84af1-114">Nome del file IotHub</span><span class="sxs-lookup"><span data-stu-id="84af1-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="84af1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84af1-115">-ResourceGroupName</span></span>
<span data-ttu-id="84af1-116">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="84af1-116">Resource Group Name</span></span>

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

### <span data-ttu-id="84af1-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="84af1-117">-Confirm</span></span>
<span data-ttu-id="84af1-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84af1-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84af1-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84af1-119">-WhatIf</span></span>
<span data-ttu-id="84af1-120">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="84af1-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84af1-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="84af1-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84af1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84af1-122">CommonParameters</span></span>
<span data-ttu-id="84af1-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84af1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84af1-124">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84af1-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84af1-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="84af1-125">INPUTS</span></span>

### <span data-ttu-id="84af1-126">System.String</span><span class="sxs-lookup"><span data-stu-id="84af1-126">System.String</span></span>

## <span data-ttu-id="84af1-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="84af1-127">OUTPUTS</span></span>

### <span data-ttu-id="84af1-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="84af1-128">System.Void</span></span>

## <span data-ttu-id="84af1-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="84af1-129">NOTES</span></span>

## <span data-ttu-id="84af1-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="84af1-130">RELATED LINKS</span></span>
