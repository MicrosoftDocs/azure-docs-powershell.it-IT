---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/remove-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayHybridConnection.md
ms.openlocfilehash: b426eda2ab7e9714cd46a95c25d248adef5464a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000462"
---
# <span data-ttu-id="08568-101">Remove-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="08568-101">Remove-AzRelayHybridConnection</span></span>

## <span data-ttu-id="08568-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08568-102">SYNOPSIS</span></span>
<span data-ttu-id="08568-103">Rimuove HybridConnection dallo spazio dei nomi HybridConnection specificato.</span><span class="sxs-lookup"><span data-stu-id="08568-103">Removes the HybridConnection from the specified HybridConnection namespace.</span></span>

## <span data-ttu-id="08568-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="08568-104">SYNTAX</span></span>

```
Remove-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08568-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="08568-105">DESCRIPTION</span></span>
<span data-ttu-id="08568-106">Il cmdlet **Remove-AzRelayHybridConnection** rimuove HybridConnection dallo spazio dei nomi Relay specificato.</span><span class="sxs-lookup"><span data-stu-id="08568-106">The **Remove-AzRelayHybridConnection** cmdlet removes the HybridConnection from the specified Relay namespace.</span></span>

## <span data-ttu-id="08568-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="08568-107">EXAMPLES</span></span>

### <span data-ttu-id="08568-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="08568-108">Example 1</span></span>
```
PS C:\> Remove-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
```

<span data-ttu-id="08568-109">Rimuove HybridConnection `TestHybridConnection` dallo spazio dei `TestNameSpace-Relay1` nomi.</span><span class="sxs-lookup"><span data-stu-id="08568-109">Removes the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="08568-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="08568-110">PARAMETERS</span></span>

### <span data-ttu-id="08568-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08568-111">-DefaultProfile</span></span>
<span data-ttu-id="08568-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="08568-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08568-113">-Name</span><span class="sxs-lookup"><span data-stu-id="08568-113">-Name</span></span>
<span data-ttu-id="08568-114">Nome HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="08568-114">HybridConnections Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08568-115">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="08568-115">-Namespace</span></span>
<span data-ttu-id="08568-116">Nome spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="08568-116">Namespace Name.</span></span>

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

### <span data-ttu-id="08568-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08568-117">-ResourceGroupName</span></span>
<span data-ttu-id="08568-118">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="08568-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="08568-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="08568-119">-Confirm</span></span>
<span data-ttu-id="08568-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08568-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08568-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08568-121">-WhatIf</span></span>
<span data-ttu-id="08568-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="08568-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08568-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="08568-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08568-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08568-124">CommonParameters</span></span>
<span data-ttu-id="08568-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08568-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08568-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08568-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08568-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="08568-127">INPUTS</span></span>

### <span data-ttu-id="08568-128">System.String</span><span class="sxs-lookup"><span data-stu-id="08568-128">System.String</span></span>

## <span data-ttu-id="08568-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="08568-129">OUTPUTS</span></span>

### <span data-ttu-id="08568-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="08568-130">System.Void</span></span>

## <span data-ttu-id="08568-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="08568-131">NOTES</span></span>

## <span data-ttu-id="08568-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="08568-132">RELATED LINKS</span></span>
