---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/remove-azurermrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 746033cfdf48782d10c0fdabf7a018d309269afb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507324"
---
# <span data-ttu-id="704f5-101">Remove-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="704f5-101">Remove-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="704f5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="704f5-102">SYNOPSIS</span></span>
<span data-ttu-id="704f5-103">Rimuove HybridConnection dallo spazio dei nomi HybridConnection specificato.</span><span class="sxs-lookup"><span data-stu-id="704f5-103">Removes the HybridConnection from the specified HybridConnection namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="704f5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="704f5-104">SYNTAX</span></span>

```
Remove-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="704f5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="704f5-105">DESCRIPTION</span></span>
<span data-ttu-id="704f5-106">Il cmdlet **Remove-AzureRmRelayHybridConnection** rimuove HybridConnection dallo spazio dei nomi Relay specificato.</span><span class="sxs-lookup"><span data-stu-id="704f5-106">The **Remove-AzureRmRelayHybridConnection** cmdlet removes the HybridConnection from the specified Relay namespace.</span></span>

## <span data-ttu-id="704f5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="704f5-107">EXAMPLES</span></span>

### <span data-ttu-id="704f5-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="704f5-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
```

<span data-ttu-id="704f5-109">Rimuove HybridConnection `TestHybridConnection` dallo spazio dei nomi `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="704f5-109">Removes the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="704f5-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="704f5-110">PARAMETERS</span></span>

### <span data-ttu-id="704f5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="704f5-111">-DefaultProfile</span></span>
<span data-ttu-id="704f5-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="704f5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="704f5-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="704f5-113">-Name</span></span>
<span data-ttu-id="704f5-114">Nome HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="704f5-114">HybridConnections Name.</span></span>

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

### <span data-ttu-id="704f5-115">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="704f5-115">-Namespace</span></span>
<span data-ttu-id="704f5-116">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="704f5-116">Namespace Name.</span></span>

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

### <span data-ttu-id="704f5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="704f5-117">-ResourceGroupName</span></span>
<span data-ttu-id="704f5-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="704f5-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="704f5-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="704f5-119">-Confirm</span></span>
<span data-ttu-id="704f5-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="704f5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="704f5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="704f5-121">-WhatIf</span></span>
<span data-ttu-id="704f5-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="704f5-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="704f5-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="704f5-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="704f5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="704f5-124">CommonParameters</span></span>
<span data-ttu-id="704f5-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="704f5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="704f5-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="704f5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="704f5-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="704f5-127">INPUTS</span></span>

### <span data-ttu-id="704f5-128">System. String</span><span class="sxs-lookup"><span data-stu-id="704f5-128">System.String</span></span>


## <span data-ttu-id="704f5-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="704f5-129">OUTPUTS</span></span>

### <span data-ttu-id="704f5-130">System. void</span><span class="sxs-lookup"><span data-stu-id="704f5-130">System.Void</span></span>


## <span data-ttu-id="704f5-131">Note</span><span class="sxs-lookup"><span data-stu-id="704f5-131">NOTES</span></span>

## <span data-ttu-id="704f5-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="704f5-132">RELATED LINKS</span></span>
