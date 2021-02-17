---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
ms.openlocfilehash: 463ef6d1d23ffe809d8810a9cbf4dd0ebf1ff578
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197999"
---
# <span data-ttu-id="8f7fc-101">Remove-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="8f7fc-101">Remove-AzRelayNamespace</span></span>

## <span data-ttu-id="8f7fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f7fc-102">SYNOPSIS</span></span>
<span data-ttu-id="8f7fc-103">Rimuove lo spazio dei nomi dal gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="8f7fc-103">Removes the namespace from the specified resource group.</span></span> 

## <span data-ttu-id="8f7fc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8f7fc-104">SYNTAX</span></span>

```
Remove-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f7fc-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8f7fc-105">DESCRIPTION</span></span>
<span data-ttu-id="8f7fc-106">Il cmdlet **Remove-AzRelaySburg** rimuove lo spazio dei nomi dal gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="8f7fc-106">The **Remove-AzRelayNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="8f7fc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8f7fc-107">EXAMPLES</span></span>

### <span data-ttu-id="8f7fc-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8f7fc-108">Example 1</span></span>
```
PS C:\> Remove-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="8f7fc-109">Rimuove lo spazio dei nomi `TestNameSpace-Relay1` Relay dal gruppo di risorse `Default-ServiceBus-WestUS` specificato.</span><span class="sxs-lookup"><span data-stu-id="8f7fc-109">Removes the Relay namespace `TestNameSpace-Relay1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="8f7fc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f7fc-110">PARAMETERS</span></span>

### <span data-ttu-id="8f7fc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f7fc-111">-DefaultProfile</span></span>
<span data-ttu-id="8f7fc-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8f7fc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f7fc-113">-Name</span><span class="sxs-lookup"><span data-stu-id="8f7fc-113">-Name</span></span>
<span data-ttu-id="8f7fc-114">Relay Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="8f7fc-114">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="8f7fc-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f7fc-115">-ResourceGroupName</span></span>
<span data-ttu-id="8f7fc-116">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8f7fc-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="8f7fc-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8f7fc-117">-Confirm</span></span>
<span data-ttu-id="8f7fc-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f7fc-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f7fc-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f7fc-119">-WhatIf</span></span>
<span data-ttu-id="8f7fc-120">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8f7fc-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f7fc-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8f7fc-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f7fc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f7fc-122">CommonParameters</span></span>
<span data-ttu-id="8f7fc-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f7fc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f7fc-124">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f7fc-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f7fc-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="8f7fc-125">INPUTS</span></span>

### <span data-ttu-id="8f7fc-126">System.String</span><span class="sxs-lookup"><span data-stu-id="8f7fc-126">System.String</span></span>

## <span data-ttu-id="8f7fc-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8f7fc-127">OUTPUTS</span></span>

### <span data-ttu-id="8f7fc-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="8f7fc-128">System.Void</span></span>

## <span data-ttu-id="8f7fc-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="8f7fc-129">NOTES</span></span>

## <span data-ttu-id="8f7fc-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8f7fc-130">RELATED LINKS</span></span>
