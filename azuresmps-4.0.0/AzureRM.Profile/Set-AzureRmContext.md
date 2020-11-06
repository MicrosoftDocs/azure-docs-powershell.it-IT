---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: e141e2af2dea2a07a9a64ab25c2417ffb6842837
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491322"
---
# <span data-ttu-id="f0e9d-101">Set-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="f0e9d-101">Set-AzureRmContext</span></span>

## <span data-ttu-id="f0e9d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f0e9d-102">SYNOPSIS</span></span>
<span data-ttu-id="f0e9d-103">Imposta il tenant, l'abbonamento e l'ambiente per i cmdlet da usare nella sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="f0e9d-103">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

## <span data-ttu-id="f0e9d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f0e9d-104">SYNTAX</span></span>

### <span data-ttu-id="f0e9d-105">Subscriptionname (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f0e9d-105">SubscriptionName (Default)</span></span>
```
Set-AzureRmContext [-SubscriptionName <String>] [-TenantId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0e9d-106">Contesto</span><span class="sxs-lookup"><span data-stu-id="f0e9d-106">Context</span></span>
```
Set-AzureRmContext -Context <PSAzureContext> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0e9d-107">SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f0e9d-107">SubscriptionId</span></span>
```
Set-AzureRmContext [-TenantId <String>] [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0e9d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f0e9d-108">DESCRIPTION</span></span>
<span data-ttu-id="f0e9d-109">Il cmdlet Set-AzureRmContext imposta le informazioni di autenticazione per i cmdlet eseguiti nella sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="f0e9d-109">The Set-AzureRmContext cmdlet sets authentication information for cmdlets that you run in the current session.</span></span>
<span data-ttu-id="f0e9d-110">Il contesto include informazioni su tenant, abbonamenti e ambiente.</span><span class="sxs-lookup"><span data-stu-id="f0e9d-110">The context includes tenant, subscription, and environment information.</span></span>

## <span data-ttu-id="f0e9d-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f0e9d-111">EXAMPLES</span></span>

### <span data-ttu-id="f0e9d-112">Esempio 1: impostare il contesto di sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="f0e9d-112">Example 1: Set the subscription context</span></span>
```
PS C:\>Set-AzureRmContext -SubscriptionId "xxxx-xxxx-xxxx-xxxx"

Account      : PFuller@contoso.com
Environment  : AzureCloud
Subscription : xxxx-xxxx-xxxx-xxxx
Tenant       : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="f0e9d-113">Questo comando imposta il contesto per l'uso della sottoscrizione specificata.</span><span class="sxs-lookup"><span data-stu-id="f0e9d-113">This command sets the context to use the specified subscription.</span></span>

## <span data-ttu-id="f0e9d-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f0e9d-114">PARAMETERS</span></span>

### <span data-ttu-id="f0e9d-115">-Contesto</span><span class="sxs-lookup"><span data-stu-id="f0e9d-115">-Context</span></span>
<span data-ttu-id="f0e9d-116">Specifica il contesto per la sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="f0e9d-116">Specifies the context for the current session.</span></span>

```yaml
Type: PSAzureContext
Parameter Sets: Context
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0e9d-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f0e9d-117">-SubscriptionId</span></span>
<span data-ttu-id="f0e9d-118">Specifica l'ID abbonamento per il contesto impostato da questo cmdlet per la sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="f0e9d-118">Specifies the subscription ID for the context that this cmdlet sets for the current session.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0e9d-119">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="f0e9d-119">-SubscriptionName</span></span>
<span data-ttu-id="f0e9d-120">Specifica il nome dell'abbonamento per il contesto impostato da questo cmdlet per la sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="f0e9d-120">Specifies the subscription name for the context that this cmdlet sets for the current session.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0e9d-121">-ID tenant</span><span class="sxs-lookup"><span data-stu-id="f0e9d-121">-TenantId</span></span>
<span data-ttu-id="f0e9d-122">Specifica l'ID del tenant per il contesto impostato da questo cmdlet per la sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="f0e9d-122">Specifies the ID of the tenant for the context that this cmdlet sets for the current session.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionName, SubscriptionId
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0e9d-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f0e9d-123">-Confirm</span></span>
<span data-ttu-id="f0e9d-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0e9d-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0e9d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0e9d-125">-WhatIf</span></span>
<span data-ttu-id="f0e9d-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f0e9d-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f0e9d-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f0e9d-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0e9d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0e9d-128">CommonParameters</span></span>
<span data-ttu-id="f0e9d-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0e9d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0e9d-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0e9d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0e9d-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f0e9d-131">INPUTS</span></span>

## <span data-ttu-id="f0e9d-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f0e9d-132">OUTPUTS</span></span>

### <span data-ttu-id="f0e9d-133">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="f0e9d-133">PSAzureContext</span></span>

## <span data-ttu-id="f0e9d-134">Note</span><span class="sxs-lookup"><span data-stu-id="f0e9d-134">NOTES</span></span>

## <span data-ttu-id="f0e9d-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f0e9d-135">RELATED LINKS</span></span>

[<span data-ttu-id="f0e9d-136">Get-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="f0e9d-136">Get-AzureRMContext</span></span>]()

