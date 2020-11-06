---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/remove-azurermwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmWcfRelay.md
ms.openlocfilehash: 5e49497f8784e9686c84cb75dde4b8fd4297578d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513528"
---
# <span data-ttu-id="5e164-101">Remove-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="5e164-101">Remove-AzureRmWcfRelay</span></span>

## <span data-ttu-id="5e164-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5e164-102">SYNOPSIS</span></span>
<span data-ttu-id="5e164-103">Rimuove WcfRelay dallo spazio dei nomi Relay specificato.</span><span class="sxs-lookup"><span data-stu-id="5e164-103">Removes the WcfRelay from the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e164-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5e164-104">SYNTAX</span></span>

```
Remove-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e164-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e164-105">DESCRIPTION</span></span>
<span data-ttu-id="5e164-106">Il cmdlet **Remove-AzureRmWcfRelay** rimuove WcfRelay dallo spazio dei nomi Relay specificato.</span><span class="sxs-lookup"><span data-stu-id="5e164-106">The **Remove-AzureRmWcfRelay** cmdlet removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="5e164-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5e164-107">EXAMPLES</span></span>

### <span data-ttu-id="5e164-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5e164-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="5e164-109">Rimuove WcfRelay `TestWCFRelay1` dallo spazio dei nomi `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="5e164-109">Removes the WcfRelay `TestWCFRelay1` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="5e164-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5e164-110">PARAMETERS</span></span>

### <span data-ttu-id="5e164-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e164-111">-DefaultProfile</span></span>
<span data-ttu-id="5e164-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5e164-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e164-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="5e164-113">-Name</span></span>
<span data-ttu-id="5e164-114">Nome WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="5e164-114">WcfRelay Name.</span></span>

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

### <span data-ttu-id="5e164-115">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5e164-115">-Namespace</span></span>
<span data-ttu-id="5e164-116">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="5e164-116">Namespace Name.</span></span>

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

### <span data-ttu-id="5e164-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e164-117">-ResourceGroupName</span></span>
<span data-ttu-id="5e164-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5e164-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="5e164-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5e164-119">-Confirm</span></span>
<span data-ttu-id="5e164-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e164-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e164-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e164-121">-WhatIf</span></span>
<span data-ttu-id="5e164-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5e164-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e164-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5e164-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e164-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e164-124">CommonParameters</span></span>
<span data-ttu-id="5e164-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e164-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5e164-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e164-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e164-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5e164-127">INPUTS</span></span>

### <span data-ttu-id="5e164-128">System. String</span><span class="sxs-lookup"><span data-stu-id="5e164-128">System.String</span></span>


## <span data-ttu-id="5e164-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5e164-129">OUTPUTS</span></span>

### <span data-ttu-id="5e164-130">System. void</span><span class="sxs-lookup"><span data-stu-id="5e164-130">System.Void</span></span>


## <span data-ttu-id="5e164-131">Note</span><span class="sxs-lookup"><span data-stu-id="5e164-131">NOTES</span></span>

## <span data-ttu-id="5e164-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5e164-132">RELATED LINKS</span></span>
