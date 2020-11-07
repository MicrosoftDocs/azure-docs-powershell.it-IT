---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayHybridConnection.md
ms.openlocfilehash: da563f063fb22ffd5c21dfc3d330a59a122c9a84
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93865116"
---
# <span data-ttu-id="37f94-101">Remove-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="37f94-101">Remove-AzRelayHybridConnection</span></span>

## <span data-ttu-id="37f94-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="37f94-102">SYNOPSIS</span></span>
<span data-ttu-id="37f94-103">Rimuove HybridConnection dallo spazio dei nomi HybridConnection specificato.</span><span class="sxs-lookup"><span data-stu-id="37f94-103">Removes the HybridConnection from the specified HybridConnection namespace.</span></span>

## <span data-ttu-id="37f94-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="37f94-104">SYNTAX</span></span>

```
Remove-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37f94-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="37f94-105">DESCRIPTION</span></span>
<span data-ttu-id="37f94-106">Il cmdlet **Remove-AzRelayHybridConnection** rimuove HybridConnection dallo spazio dei nomi Relay specificato.</span><span class="sxs-lookup"><span data-stu-id="37f94-106">The **Remove-AzRelayHybridConnection** cmdlet removes the HybridConnection from the specified Relay namespace.</span></span>

## <span data-ttu-id="37f94-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="37f94-107">EXAMPLES</span></span>

### <span data-ttu-id="37f94-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="37f94-108">Example 1</span></span>
```
PS C:\> Remove-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
```

<span data-ttu-id="37f94-109">Rimuove HybridConnection `TestHybridConnection` dallo spazio dei nomi `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="37f94-109">Removes the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="37f94-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="37f94-110">PARAMETERS</span></span>

### <span data-ttu-id="37f94-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37f94-111">-DefaultProfile</span></span>
<span data-ttu-id="37f94-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="37f94-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37f94-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="37f94-113">-Name</span></span>
<span data-ttu-id="37f94-114">Nome HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="37f94-114">HybridConnections Name.</span></span>

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

### <span data-ttu-id="37f94-115">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="37f94-115">-Namespace</span></span>
<span data-ttu-id="37f94-116">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="37f94-116">Namespace Name.</span></span>

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

### <span data-ttu-id="37f94-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37f94-117">-ResourceGroupName</span></span>
<span data-ttu-id="37f94-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="37f94-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="37f94-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="37f94-119">-Confirm</span></span>
<span data-ttu-id="37f94-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37f94-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37f94-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37f94-121">-WhatIf</span></span>
<span data-ttu-id="37f94-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="37f94-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37f94-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="37f94-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37f94-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37f94-124">CommonParameters</span></span>
<span data-ttu-id="37f94-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37f94-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37f94-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37f94-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37f94-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="37f94-127">INPUTS</span></span>

### <span data-ttu-id="37f94-128">System. String</span><span class="sxs-lookup"><span data-stu-id="37f94-128">System.String</span></span>

## <span data-ttu-id="37f94-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="37f94-129">OUTPUTS</span></span>

### <span data-ttu-id="37f94-130">System. void</span><span class="sxs-lookup"><span data-stu-id="37f94-130">System.Void</span></span>

## <span data-ttu-id="37f94-131">Note</span><span class="sxs-lookup"><span data-stu-id="37f94-131">NOTES</span></span>

## <span data-ttu-id="37f94-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="37f94-132">RELATED LINKS</span></span>
