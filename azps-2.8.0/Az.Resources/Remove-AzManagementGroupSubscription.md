---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupSubscription.md
ms.openlocfilehash: a193312379aee69e0256975681ab8eb867e41c8e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854801"
---
# <span data-ttu-id="c1143-101">Remove-AzManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="c1143-101">Remove-AzManagementGroupSubscription</span></span>

## <span data-ttu-id="c1143-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c1143-102">SYNOPSIS</span></span>
<span data-ttu-id="c1143-103">Rimuove un abbonamento da un gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="c1143-103">Removes a Subscription from a Management Group.</span></span>

## <span data-ttu-id="c1143-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c1143-104">SYNTAX</span></span>

```
Remove-AzManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1143-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c1143-105">DESCRIPTION</span></span>
<span data-ttu-id="c1143-106">Il cmdlet **Remove-AzManagementGroupSubscription** rimuove un abbonamento da un gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="c1143-106">The **Remove-AzManagementGroupSubscription** cmdlet removes a Subscription from a Management Group.</span></span>

## <span data-ttu-id="c1143-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c1143-107">EXAMPLES</span></span>

### <span data-ttu-id="c1143-108">Esempio 1-rimuovere l'abbonamento da un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="c1143-108">Example 1 - Remove Subscription from a Management Group</span></span>
```
PS C:\> Remove-AzManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="c1143-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c1143-109">PARAMETERS</span></span>

### <span data-ttu-id="c1143-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1143-110">-DefaultProfile</span></span>
<span data-ttu-id="c1143-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c1143-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1143-112">-GroupName</span><span class="sxs-lookup"><span data-stu-id="c1143-112">-GroupName</span></span>
<span data-ttu-id="c1143-113">ID gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="c1143-113">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1143-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c1143-114">-PassThru</span></span>
<span data-ttu-id="c1143-115">Ritorno `true` all'esecuzione completata</span><span class="sxs-lookup"><span data-stu-id="c1143-115">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="c1143-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c1143-116">-SubscriptionId</span></span>
<span data-ttu-id="c1143-117">ID sottoscrizione dell'abbonamento associato alla gestione</span><span class="sxs-lookup"><span data-stu-id="c1143-117">Subscription Id of the subscription associated with the management</span></span>

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

### <span data-ttu-id="c1143-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c1143-118">-Confirm</span></span>
<span data-ttu-id="c1143-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1143-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1143-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1143-120">-WhatIf</span></span>
<span data-ttu-id="c1143-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c1143-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1143-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c1143-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1143-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1143-123">CommonParameters</span></span>
<span data-ttu-id="c1143-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1143-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1143-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1143-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1143-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c1143-126">INPUTS</span></span>

### <span data-ttu-id="c1143-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c1143-127">None</span></span>

## <span data-ttu-id="c1143-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c1143-128">OUTPUTS</span></span>

### <span data-ttu-id="c1143-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c1143-129">System.Boolean</span></span>

## <span data-ttu-id="c1143-130">Note</span><span class="sxs-lookup"><span data-stu-id="c1143-130">NOTES</span></span>

## <span data-ttu-id="c1143-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c1143-131">RELATED LINKS</span></span>
