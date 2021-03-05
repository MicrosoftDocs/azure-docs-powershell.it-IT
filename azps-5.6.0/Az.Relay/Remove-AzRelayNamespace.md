---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/remove-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
ms.openlocfilehash: 17a5cb5c05b9bd3293b15ef48b90c8d7387744da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000461"
---
# <span data-ttu-id="4cd82-101">Remove-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="4cd82-101">Remove-AzRelayNamespace</span></span>

## <span data-ttu-id="4cd82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cd82-102">SYNOPSIS</span></span>
<span data-ttu-id="4cd82-103">Rimuove lo spazio dei nomi dal gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="4cd82-103">Removes the namespace from the specified resource group.</span></span> 

## <span data-ttu-id="4cd82-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4cd82-104">SYNTAX</span></span>

```
Remove-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cd82-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4cd82-105">DESCRIPTION</span></span>
<span data-ttu-id="4cd82-106">Il cmdlet **Remove-AzRelay Env rimuove** lo spazio dei nomi dal gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="4cd82-106">The **Remove-AzRelayNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="4cd82-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4cd82-107">EXAMPLES</span></span>

### <span data-ttu-id="4cd82-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4cd82-108">Example 1</span></span>
```
PS C:\> Remove-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="4cd82-109">Rimuove lo spazio dei nomi `TestNameSpace-Relay1` Relay dal gruppo di risorse `Default-ServiceBus-WestUS` specificato.</span><span class="sxs-lookup"><span data-stu-id="4cd82-109">Removes the Relay namespace `TestNameSpace-Relay1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="4cd82-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4cd82-110">PARAMETERS</span></span>

### <span data-ttu-id="4cd82-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cd82-111">-DefaultProfile</span></span>
<span data-ttu-id="4cd82-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4cd82-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cd82-113">-Name</span><span class="sxs-lookup"><span data-stu-id="4cd82-113">-Name</span></span>
<span data-ttu-id="4cd82-114">Nome spazio dei nomi di inoltro.</span><span class="sxs-lookup"><span data-stu-id="4cd82-114">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="4cd82-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cd82-115">-ResourceGroupName</span></span>
<span data-ttu-id="4cd82-116">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4cd82-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="4cd82-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4cd82-117">-Confirm</span></span>
<span data-ttu-id="4cd82-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cd82-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cd82-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cd82-119">-WhatIf</span></span>
<span data-ttu-id="4cd82-120">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4cd82-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cd82-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4cd82-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cd82-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cd82-122">CommonParameters</span></span>
<span data-ttu-id="4cd82-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cd82-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cd82-124">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cd82-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cd82-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="4cd82-125">INPUTS</span></span>

### <span data-ttu-id="4cd82-126">System.String</span><span class="sxs-lookup"><span data-stu-id="4cd82-126">System.String</span></span>

## <span data-ttu-id="4cd82-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4cd82-127">OUTPUTS</span></span>

### <span data-ttu-id="4cd82-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="4cd82-128">System.Void</span></span>

## <span data-ttu-id="4cd82-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="4cd82-129">NOTES</span></span>

## <span data-ttu-id="4cd82-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4cd82-130">RELATED LINKS</span></span>
