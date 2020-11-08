---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
ms.openlocfilehash: 463ef6d1d23ffe809d8810a9cbf4dd0ebf1ff578
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190658"
---
# <span data-ttu-id="db237-101">Remove-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="db237-101">Remove-AzRelayNamespace</span></span>

## <span data-ttu-id="db237-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="db237-102">SYNOPSIS</span></span>
<span data-ttu-id="db237-103">Rimuove lo spazio dei nomi dal gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="db237-103">Removes the namespace from the specified resource group.</span></span> 

## <span data-ttu-id="db237-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db237-104">SYNTAX</span></span>

```
Remove-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db237-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db237-105">DESCRIPTION</span></span>
<span data-ttu-id="db237-106">Il cmdlet **Remove-AzRelayNamespace** rimuove lo spazio dei nomi dal gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="db237-106">The **Remove-AzRelayNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="db237-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db237-107">EXAMPLES</span></span>

### <span data-ttu-id="db237-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="db237-108">Example 1</span></span>
```
PS C:\> Remove-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="db237-109">Rimuove lo spazio dei nomi Relay `TestNameSpace-Relay1` dal gruppo di risorse specificato `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="db237-109">Removes the Relay namespace `TestNameSpace-Relay1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="db237-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="db237-110">PARAMETERS</span></span>

### <span data-ttu-id="db237-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db237-111">-DefaultProfile</span></span>
<span data-ttu-id="db237-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="db237-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db237-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="db237-113">-Name</span></span>
<span data-ttu-id="db237-114">Nome dello spazio dei nomi Relay.</span><span class="sxs-lookup"><span data-stu-id="db237-114">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="db237-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db237-115">-ResourceGroupName</span></span>
<span data-ttu-id="db237-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="db237-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="db237-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="db237-117">-Confirm</span></span>
<span data-ttu-id="db237-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db237-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db237-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db237-119">-WhatIf</span></span>
<span data-ttu-id="db237-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db237-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db237-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db237-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db237-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db237-122">CommonParameters</span></span>
<span data-ttu-id="db237-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db237-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db237-124">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db237-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db237-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="db237-125">INPUTS</span></span>

### <span data-ttu-id="db237-126">System. String</span><span class="sxs-lookup"><span data-stu-id="db237-126">System.String</span></span>

## <span data-ttu-id="db237-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db237-127">OUTPUTS</span></span>

### <span data-ttu-id="db237-128">System. void</span><span class="sxs-lookup"><span data-stu-id="db237-128">System.Void</span></span>

## <span data-ttu-id="db237-129">Note</span><span class="sxs-lookup"><span data-stu-id="db237-129">NOTES</span></span>

## <span data-ttu-id="db237-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db237-130">RELATED LINKS</span></span>