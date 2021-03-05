---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
ms.openlocfilehash: aea1b80507b753a84afd9228c4845da973273a37
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978989"
---
# <span data-ttu-id="16230-101">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="16230-101">Set-AzApiManagementSubscription</span></span>

## <span data-ttu-id="16230-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16230-102">SYNOPSIS</span></span>
<span data-ttu-id="16230-103">Imposta i dettagli dell'abbonamento esistente.</span><span class="sxs-lookup"><span data-stu-id="16230-103">Sets existing subscription details.</span></span>

## <span data-ttu-id="16230-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="16230-104">SYNTAX</span></span>

### <span data-ttu-id="16230-105">ByInputObject (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="16230-105">ByInputObject (Default)</span></span>
```
Set-AzApiManagementSubscription -InputObject <PsApiManagementSubscription> [-Scope <String>] [-UserId <String>]
 [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16230-106">ExpandedParameter</span><span class="sxs-lookup"><span data-stu-id="16230-106">ExpandedParameter</span></span>
```
Set-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-Scope <String>]
 [-UserId <String>] [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16230-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="16230-107">DESCRIPTION</span></span>
<span data-ttu-id="16230-108">Il cmdlet **Set-AzApiManagementSubscription** imposta i dettagli della sottoscrizione esistente.</span><span class="sxs-lookup"><span data-stu-id="16230-108">The **Set-AzApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="16230-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="16230-109">EXAMPLES</span></span>

### <span data-ttu-id="16230-110">Esempio 1: Impostare lo stato e le chiavi primaria e secondaria per un abbonamento</span><span class="sxs-lookup"><span data-stu-id="16230-110">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SecondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="16230-111">Questo comando imposta i tasti primario e secondario per un abbonamento e lo attiva.</span><span class="sxs-lookup"><span data-stu-id="16230-111">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="16230-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16230-112">PARAMETERS</span></span>

### <span data-ttu-id="16230-113">-Context</span><span class="sxs-lookup"><span data-stu-id="16230-113">-Context</span></span>
<span data-ttu-id="16230-114">Specifica un **oggetto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="16230-114">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16230-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16230-115">-DefaultProfile</span></span>
<span data-ttu-id="16230-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="16230-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16230-117">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="16230-117">-ExpiresOn</span></span>
<span data-ttu-id="16230-118">Specifica la data di scadenza di un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="16230-118">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="16230-119">Il valore predefinito di questo parametro è $Null.</span><span class="sxs-lookup"><span data-stu-id="16230-119">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16230-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16230-120">-InputObject</span></span>
<span data-ttu-id="16230-121">Istanza di PsApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="16230-121">Instance of PsApiManagementSubscription.</span></span> <span data-ttu-id="16230-122">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="16230-122">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16230-123">-Name</span><span class="sxs-lookup"><span data-stu-id="16230-123">-Name</span></span>
<span data-ttu-id="16230-124">Specifica il nome di un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="16230-124">Specifies a subscription name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16230-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="16230-125">-PassThru</span></span>
<span data-ttu-id="16230-126">passthru</span><span class="sxs-lookup"><span data-stu-id="16230-126">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16230-127">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="16230-127">-PrimaryKey</span></span>
<span data-ttu-id="16230-128">Specifica la chiave primaria dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="16230-128">Specifies the subscription primary key.</span></span>
<span data-ttu-id="16230-129">Questo parametro viene generato automaticamente se non viene specificato.</span><span class="sxs-lookup"><span data-stu-id="16230-129">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="16230-130">Questo parametro deve contenere da 1 a 300 caratteri.</span><span class="sxs-lookup"><span data-stu-id="16230-130">This parameter must be 1 to 300 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16230-131">-Scope</span><span class="sxs-lookup"><span data-stu-id="16230-131">-Scope</span></span>
<span data-ttu-id="16230-132">Ambito della Sottoscrizione, che si tratta di Ambito API /api/{apiId} o Ambito prodotto /products/{productId} o Ambito API globale /api o Ambito globale /.</span><span class="sxs-lookup"><span data-stu-id="16230-132">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span> <span data-ttu-id="16230-133">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="16230-133">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16230-134">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="16230-134">-SecondaryKey</span></span>
<span data-ttu-id="16230-135">Specifica la chiave secondaria di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="16230-135">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="16230-136">Questo parametro viene generato automaticamente se non viene specificato.</span><span class="sxs-lookup"><span data-stu-id="16230-136">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="16230-137">Questo parametro deve contenere da 1 a 300 caratteri.</span><span class="sxs-lookup"><span data-stu-id="16230-137">This parameter must be 1 to 300 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16230-138">-State</span><span class="sxs-lookup"><span data-stu-id="16230-138">-State</span></span>
<span data-ttu-id="16230-139">Specifica lo stato della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="16230-139">Specifies the subscription state.</span></span>
<span data-ttu-id="16230-140">Il valore predefinito di questo parametro è $Null.</span><span class="sxs-lookup"><span data-stu-id="16230-140">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState]
Parameter Sets: (All)
Aliases:
Accepted values: Suspended, Active, Expired, Submitted, Rejected, Cancelled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16230-141">-StateComment</span><span class="sxs-lookup"><span data-stu-id="16230-141">-StateComment</span></span>
<span data-ttu-id="16230-142">Specifica il commento sullo stato della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="16230-142">Specifies the subscription state comment.</span></span>
<span data-ttu-id="16230-143">Il valore predefinito di questo parametro è $Null.</span><span class="sxs-lookup"><span data-stu-id="16230-143">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16230-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="16230-144">-SubscriptionId</span></span>
<span data-ttu-id="16230-145">Specifica l'ID sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="16230-145">Specifies the subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16230-146">-UserId</span><span class="sxs-lookup"><span data-stu-id="16230-146">-UserId</span></span>
<span data-ttu-id="16230-147">Proprietario della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="16230-147">The owner of the subscription.</span></span> <span data-ttu-id="16230-148">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="16230-148">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16230-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="16230-149">-Confirm</span></span>
<span data-ttu-id="16230-150">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16230-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16230-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16230-151">-WhatIf</span></span>
<span data-ttu-id="16230-152">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="16230-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="16230-153">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="16230-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16230-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16230-154">CommonParameters</span></span>
<span data-ttu-id="16230-155">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16230-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16230-156">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="16230-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16230-157">INPUT</span><span class="sxs-lookup"><span data-stu-id="16230-157">INPUTS</span></span>

### <span data-ttu-id="16230-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="16230-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="16230-159">System.String</span><span class="sxs-lookup"><span data-stu-id="16230-159">System.String</span></span>

### <span data-ttu-id="16230-160">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="16230-160">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="16230-161">System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="16230-161">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="16230-162">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="16230-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="16230-163">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="16230-163">OUTPUTS</span></span>

### <span data-ttu-id="16230-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="16230-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="16230-165">NOTE</span><span class="sxs-lookup"><span data-stu-id="16230-165">NOTES</span></span>

## <span data-ttu-id="16230-166">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="16230-166">RELATED LINKS</span></span>

[<span data-ttu-id="16230-167">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="16230-167">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="16230-168">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="16230-168">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="16230-169">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="16230-169">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)


