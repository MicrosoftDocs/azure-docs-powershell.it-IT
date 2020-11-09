---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupSubscription.md
ms.openlocfilehash: 39325462d9c2cfb9c06296ff98e5595d2c2c2c06
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300204"
---
# <span data-ttu-id="7a05a-101">New-AzManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="7a05a-101">New-AzManagementGroupSubscription</span></span>

## <span data-ttu-id="7a05a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7a05a-102">SYNOPSIS</span></span>
<span data-ttu-id="7a05a-103">Aggiunge una sottoscrizione a un gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="7a05a-103">Adds a Subscription to a Management Group.</span></span>

## <span data-ttu-id="7a05a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7a05a-104">SYNTAX</span></span>

```
New-AzManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a05a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a05a-105">DESCRIPTION</span></span>
<span data-ttu-id="7a05a-106">Il cmdlet **New-AzManagementGroupSubscription** aggiunge una sottoscrizione a un gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="7a05a-106">The **New-AzManagementGroupSubscription** cmdlet adds a Subscription to a Management Group.</span></span>

## <span data-ttu-id="7a05a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7a05a-107">EXAMPLES</span></span>

### <span data-ttu-id="7a05a-108">Esempio 1: aggiungere una sottoscrizione a un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="7a05a-108">Example 1: Add Subscription to a Management Group</span></span>
```
PS C:\> New-AzManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="7a05a-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7a05a-109">PARAMETERS</span></span>

### <span data-ttu-id="7a05a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a05a-110">-DefaultProfile</span></span>
<span data-ttu-id="7a05a-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7a05a-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a05a-112">-GroupName</span><span class="sxs-lookup"><span data-stu-id="7a05a-112">-GroupName</span></span>
<span data-ttu-id="7a05a-113">ID gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="7a05a-113">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a05a-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a05a-114">-PassThru</span></span>
<span data-ttu-id="7a05a-115">Ritorno `true` all'esecuzione completata</span><span class="sxs-lookup"><span data-stu-id="7a05a-115">Return `true` on successful execution</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a05a-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7a05a-116">-SubscriptionId</span></span>
<span data-ttu-id="7a05a-117">ID sottoscrizione dell'abbonamento associato alla gestione</span><span class="sxs-lookup"><span data-stu-id="7a05a-117">Subscription Id of the subscription associated with the management</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a05a-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7a05a-118">-Confirm</span></span>
<span data-ttu-id="7a05a-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a05a-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a05a-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a05a-120">-WhatIf</span></span>
<span data-ttu-id="7a05a-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7a05a-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a05a-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7a05a-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a05a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a05a-123">CommonParameters</span></span>
<span data-ttu-id="7a05a-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a05a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a05a-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a05a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a05a-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7a05a-126">INPUTS</span></span>

### <span data-ttu-id="7a05a-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7a05a-127">None</span></span>

## <span data-ttu-id="7a05a-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7a05a-128">OUTPUTS</span></span>

### <span data-ttu-id="7a05a-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7a05a-129">System.Boolean</span></span>

## <span data-ttu-id="7a05a-130">Note</span><span class="sxs-lookup"><span data-stu-id="7a05a-130">NOTES</span></span>

## <span data-ttu-id="7a05a-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7a05a-131">RELATED LINKS</span></span>
