---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/set-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmContext.md
ms.openlocfilehash: bffd818df21be78d0418bf3d2ac1ebea401dbf19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520420"
---
# <span data-ttu-id="9470c-101">Set-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="9470c-101">Set-AzureRmContext</span></span>

## <span data-ttu-id="9470c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9470c-102">SYNOPSIS</span></span>
<span data-ttu-id="9470c-103">Imposta il tenant, l'abbonamento e l'ambiente per i cmdlet da usare nella sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="9470c-103">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9470c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9470c-104">SYNTAX</span></span>

### <span data-ttu-id="9470c-105">Context (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9470c-105">Context (Default)</span></span>
```
Set-AzureRmContext [-Context] <PSAzureContext>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9470c-106">TenantObject</span><span class="sxs-lookup"><span data-stu-id="9470c-106">TenantObject</span></span>
```
Set-AzureRmContext [-TenantObject] <PSAzureTenant>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9470c-107">SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="9470c-107">SubscriptionObject</span></span>
```
Set-AzureRmContext [-SubscriptionObject] <PSAzureSubscription>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9470c-108">Abbonamento</span><span class="sxs-lookup"><span data-stu-id="9470c-108">Subscription</span></span>
```
Set-AzureRmContext [-Tenant <String>] [-Subscription] <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9470c-109">TenantNameOnly</span><span class="sxs-lookup"><span data-stu-id="9470c-109">TenantNameOnly</span></span>
```
Set-AzureRmContext -Tenant <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9470c-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9470c-110">DESCRIPTION</span></span>
<span data-ttu-id="9470c-111">Il cmdlet Set-AzureRmContext imposta le informazioni di autenticazione per i cmdlet eseguiti nella sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="9470c-111">The Set-AzureRmContext cmdlet sets authentication information for cmdlets that you run in the current session.</span></span>
<span data-ttu-id="9470c-112">Il contesto include informazioni su tenant, abbonamenti e ambiente.</span><span class="sxs-lookup"><span data-stu-id="9470c-112">The context includes tenant, subscription, and environment information.</span></span>

## <span data-ttu-id="9470c-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9470c-113">EXAMPLES</span></span>

### <span data-ttu-id="9470c-114">Esempio 1: impostare il contesto di sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="9470c-114">Example 1: Set the subscription context</span></span>
```
PS C:\>Set-AzureRmContext -SubscriptionId "xxxx-xxxx-xxxx-xxxx"

Account      : PFuller@contoso.com
Environment  : AzureCloud
Subscription : xxxx-xxxx-xxxx-xxxx
Tenant       : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="9470c-115">Questo comando imposta il contesto per l'uso della sottoscrizione specificata.</span><span class="sxs-lookup"><span data-stu-id="9470c-115">This command sets the context to use the specified subscription.</span></span>

## <span data-ttu-id="9470c-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9470c-116">PARAMETERS</span></span>

### <span data-ttu-id="9470c-117">-Contesto</span><span class="sxs-lookup"><span data-stu-id="9470c-117">-Context</span></span>
<span data-ttu-id="9470c-118">Specifica il contesto per la sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="9470c-118">Specifies the context for the current session.</span></span>

```yaml
Type: PSAzureContext
Parameter Sets: Context
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9470c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9470c-119">-DefaultProfile</span></span>
<span data-ttu-id="9470c-120">Le credenziali, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9470c-120">The credentials, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9470c-121">-ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="9470c-121">-ExtendedProperty</span></span>
<span data-ttu-id="9470c-122">Proprietà di contesto aggiuntive</span><span class="sxs-lookup"><span data-stu-id="9470c-122">Additional context properties</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9470c-123">-Force</span><span class="sxs-lookup"><span data-stu-id="9470c-123">-Force</span></span>
<span data-ttu-id="9470c-124">Sovrascrivere il contesto esistente con lo stesso nome, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="9470c-124">Overwrite the existing context with the same name, if any.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9470c-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="9470c-125">-Name</span></span>
<span data-ttu-id="9470c-126">Nome del contesto</span><span class="sxs-lookup"><span data-stu-id="9470c-126">Name of the context</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9470c-127">-Ambito</span><span class="sxs-lookup"><span data-stu-id="9470c-127">-Scope</span></span>
<span data-ttu-id="9470c-128">Determina l'ambito delle modifiche al contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate da questo utente.</span><span class="sxs-lookup"><span data-stu-id="9470c-128">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9470c-129">-Sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="9470c-129">-Subscription</span></span>
<span data-ttu-id="9470c-130">Nome dell'abbonamento o ID</span><span class="sxs-lookup"><span data-stu-id="9470c-130">Subscription Name or Id</span></span>

```yaml
Type: String
Parameter Sets: Subscription
Aliases: SubscriptionId, SubscriptionName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9470c-131">-SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="9470c-131">-SubscriptionObject</span></span>
<span data-ttu-id="9470c-132">Un oggetto Subscription</span><span class="sxs-lookup"><span data-stu-id="9470c-132">A subscription object</span></span>

```yaml
Type: PSAzureSubscription
Parameter Sets: SubscriptionObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9470c-133">-Tenant</span><span class="sxs-lookup"><span data-stu-id="9470c-133">-Tenant</span></span>
<span data-ttu-id="9470c-134">Nome del tenant o ID</span><span class="sxs-lookup"><span data-stu-id="9470c-134">Tenant name or ID</span></span>

```yaml
Type: String
Parameter Sets: Subscription
Aliases: Domain, TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: TenantNameOnly
Aliases: Domain, TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9470c-135">-TenantObject</span><span class="sxs-lookup"><span data-stu-id="9470c-135">-TenantObject</span></span>
<span data-ttu-id="9470c-136">Un oggetto tenant</span><span class="sxs-lookup"><span data-stu-id="9470c-136">A Tenant Object</span></span>

```yaml
Type: PSAzureTenant
Parameter Sets: TenantObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9470c-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9470c-137">-Confirm</span></span>
<span data-ttu-id="9470c-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9470c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9470c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9470c-139">-WhatIf</span></span>
<span data-ttu-id="9470c-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9470c-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9470c-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9470c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9470c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9470c-142">CommonParameters</span></span>
<span data-ttu-id="9470c-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9470c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9470c-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9470c-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9470c-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9470c-145">INPUTS</span></span>

### <span data-ttu-id="9470c-146">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="9470c-146">PSAzureContext</span></span>
<span data-ttu-id="9470c-147">Il parametro "context" accetta il valore di tipo "PSAzureContext" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="9470c-147">Parameter 'Context' accepts value of type 'PSAzureContext' from the pipeline</span></span>

## <span data-ttu-id="9470c-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9470c-148">OUTPUTS</span></span>

### <span data-ttu-id="9470c-149">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="9470c-149">PSAzureContext</span></span>

## <span data-ttu-id="9470c-150">Note</span><span class="sxs-lookup"><span data-stu-id="9470c-150">NOTES</span></span>

## <span data-ttu-id="9470c-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9470c-151">RELATED LINKS</span></span>

[<span data-ttu-id="9470c-152">Get-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="9470c-152">Get-AzureRMContext</span></span>](./Get-AzureRMContext.md)

