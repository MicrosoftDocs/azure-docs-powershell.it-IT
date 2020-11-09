---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzWcfRelay.md
ms.openlocfilehash: 238c4ecf92cbdd1dc6e9e0a430ec8e6ad200b967
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302557"
---
# <span data-ttu-id="07e3a-101">Remove-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="07e3a-101">Remove-AzWcfRelay</span></span>

## <span data-ttu-id="07e3a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="07e3a-102">SYNOPSIS</span></span>
<span data-ttu-id="07e3a-103">Rimuove WcfRelay dallo spazio dei nomi Relay specificato.</span><span class="sxs-lookup"><span data-stu-id="07e3a-103">Removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="07e3a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="07e3a-104">SYNTAX</span></span>

```
Remove-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07e3a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07e3a-105">DESCRIPTION</span></span>
<span data-ttu-id="07e3a-106">Il cmdlet **Remove-AzWcfRelay** rimuove WcfRelay dallo spazio dei nomi Relay specificato.</span><span class="sxs-lookup"><span data-stu-id="07e3a-106">The **Remove-AzWcfRelay** cmdlet removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="07e3a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="07e3a-107">EXAMPLES</span></span>

### <span data-ttu-id="07e3a-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="07e3a-108">Example 1</span></span>
```
PS C:\> Remove-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="07e3a-109">Rimuove WcfRelay `TestWCFRelay1` dallo spazio dei nomi `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="07e3a-109">Removes the WcfRelay `TestWCFRelay1` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="07e3a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="07e3a-110">PARAMETERS</span></span>

### <span data-ttu-id="07e3a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07e3a-111">-DefaultProfile</span></span>
<span data-ttu-id="07e3a-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="07e3a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07e3a-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="07e3a-113">-Name</span></span>
<span data-ttu-id="07e3a-114">Nome WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="07e3a-114">WcfRelay Name.</span></span>

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

### <span data-ttu-id="07e3a-115">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="07e3a-115">-Namespace</span></span>
<span data-ttu-id="07e3a-116">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="07e3a-116">Namespace Name.</span></span>

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

### <span data-ttu-id="07e3a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07e3a-117">-ResourceGroupName</span></span>
<span data-ttu-id="07e3a-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="07e3a-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="07e3a-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="07e3a-119">-Confirm</span></span>
<span data-ttu-id="07e3a-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07e3a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07e3a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07e3a-121">-WhatIf</span></span>
<span data-ttu-id="07e3a-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="07e3a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07e3a-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="07e3a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07e3a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07e3a-124">CommonParameters</span></span>
<span data-ttu-id="07e3a-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07e3a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07e3a-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07e3a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07e3a-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="07e3a-127">INPUTS</span></span>

### <span data-ttu-id="07e3a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="07e3a-128">System.String</span></span>

## <span data-ttu-id="07e3a-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="07e3a-129">OUTPUTS</span></span>

### <span data-ttu-id="07e3a-130">System. void</span><span class="sxs-lookup"><span data-stu-id="07e3a-130">System.Void</span></span>

## <span data-ttu-id="07e3a-131">Note</span><span class="sxs-lookup"><span data-stu-id="07e3a-131">NOTES</span></span>

## <span data-ttu-id="07e3a-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="07e3a-132">RELATED LINKS</span></span>
