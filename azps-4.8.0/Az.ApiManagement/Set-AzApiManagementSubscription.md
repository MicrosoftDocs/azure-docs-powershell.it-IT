---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
ms.openlocfilehash: 82c49524566293adcd8dcbdcb36359e83360158c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190616"
---
# <span data-ttu-id="0eeeb-101">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="0eeeb-101">Set-AzApiManagementSubscription</span></span>

## <span data-ttu-id="0eeeb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0eeeb-102">SYNOPSIS</span></span>
<span data-ttu-id="0eeeb-103">Imposta i dettagli degli abbonamenti esistenti.</span><span class="sxs-lookup"><span data-stu-id="0eeeb-103">Sets existing subscription details.</span></span>

## <span data-ttu-id="0eeeb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0eeeb-104">SYNTAX</span></span>

### <span data-ttu-id="0eeeb-105">ByInputObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0eeeb-105">ByInputObject (Default)</span></span>
```
Set-AzApiManagementSubscription -InputObject <PsApiManagementSubscription> [-Scope <String>] [-UserId <String>]
 [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0eeeb-106">ExpandedParameter</span><span class="sxs-lookup"><span data-stu-id="0eeeb-106">ExpandedParameter</span></span>
```
Set-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-Scope <String>]
 [-UserId <String>] [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0eeeb-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0eeeb-107">DESCRIPTION</span></span>
<span data-ttu-id="0eeeb-108">Il cmdlet **set-AzApiManagementSubscription** imposta i dettagli di sottoscrizione esistenti.</span><span class="sxs-lookup"><span data-stu-id="0eeeb-108">The **Set-AzApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="0eeeb-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0eeeb-109">EXAMPLES</span></span>

### <span data-ttu-id="0eeeb-110">Esempio 1: impostare lo stato e le chiavi primarie e secondarie per un abbonamento</span><span class="sxs-lookup"><span data-stu-id="0eeeb-110">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SecondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="0eeeb-111">Questo comando imposta le chiavi primarie e secondarie per un abbonamento e lo attiva.</span><span class="sxs-lookup"><span data-stu-id="0eeeb-111">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="0eeeb-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0eeeb-112">PARAMETERS</span></span>

### <span data-ttu-id="0eeeb-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="0eeeb-113">-Context</span></span>
<span data-ttu-id="0eeeb-114">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="0eeeb-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="0eeeb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eeeb-115">-DefaultProfile</span></span>
<span data-ttu-id="0eeeb-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0eeeb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0eeeb-117">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="0eeeb-117">-ExpiresOn</span></span>
<span data-ttu-id="0eeeb-118">Specifica una data di scadenza dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="0eeeb-118">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="0eeeb-119">Il valore predefinito di questo parametro è $Null.</span><span class="sxs-lookup"><span data-stu-id="0eeeb-119">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="0eeeb-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0eeeb-120">-InputObject</span></span>
<span data-ttu-id="0eeeb-121">Istanza di PsApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="0eeeb-121">Instance of PsApiManagementSubscription.</span></span> <span data-ttu-id="0eeeb-122">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="0eeeb-122">This parameter is required.</span></span>

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

### <span data-ttu-id="0eeeb-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="0eeeb-123">-Name</span></span>
<span data-ttu-id="0eeeb-124">Specifica un nome di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="0eeeb-124">Specifies a subscription name.</span></span>

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

### <span data-ttu-id="0eeeb-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0eeeb-125">-PassThru</span></span>
<span data-ttu-id="0eeeb-126">PassThru</span><span class="sxs-lookup"><span data-stu-id="0eeeb-126">passthru</span></span>

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

### <span data-ttu-id="0eeeb-127">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="0eeeb-127">-PrimaryKey</span></span>
<span data-ttu-id="0eeeb-128">Specifica la chiave primaria dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="0eeeb-128">Specifies the subscription primary key.</span></span>
<span data-ttu-id="0eeeb-129">Questo parametro viene generato automaticamente se non specificato.</span><span class="sxs-lookup"><span data-stu-id="0eeeb-129">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="0eeeb-130">Questo parametro deve essere lungo da 1 a 300 caratteri.</span><span class="sxs-lookup"><span data-stu-id="0eeeb-130">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="0eeeb-131">-Ambito</span><span class="sxs-lookup"><span data-stu-id="0eeeb-131">-Scope</span></span>
<span data-ttu-id="0eeeb-132">L'ambito della sottoscrizione, sia che si tratti di ambito API/apis/{apiId} o ambito prodotto/products/{productId} o ambito API globale/Apis o ambito globale/.</span><span class="sxs-lookup"><span data-stu-id="0eeeb-132">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span> <span data-ttu-id="0eeeb-133">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="0eeeb-133">This parameter is required.</span></span>

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

### <span data-ttu-id="0eeeb-134">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="0eeeb-134">-SecondaryKey</span></span>
<span data-ttu-id="0eeeb-135">Specifica la chiave secondaria dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="0eeeb-135">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="0eeeb-136">Questo parametro viene generato automaticamente se non specificato.</span><span class="sxs-lookup"><span data-stu-id="0eeeb-136">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="0eeeb-137">Questo parametro deve essere lungo da 1 a 300 caratteri.</span><span class="sxs-lookup"><span data-stu-id="0eeeb-137">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="0eeeb-138">-Stato</span><span class="sxs-lookup"><span data-stu-id="0eeeb-138">-State</span></span>
<span data-ttu-id="0eeeb-139">Specifica lo stato dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="0eeeb-139">Specifies the subscription state.</span></span>
<span data-ttu-id="0eeeb-140">Il valore predefinito di questo parametro è $Null.</span><span class="sxs-lookup"><span data-stu-id="0eeeb-140">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="0eeeb-141">-StateComment</span><span class="sxs-lookup"><span data-stu-id="0eeeb-141">-StateComment</span></span>
<span data-ttu-id="0eeeb-142">Specifica il commento sullo stato dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="0eeeb-142">Specifies the subscription state comment.</span></span>
<span data-ttu-id="0eeeb-143">Il valore predefinito di questo parametro è $Null.</span><span class="sxs-lookup"><span data-stu-id="0eeeb-143">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="0eeeb-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0eeeb-144">-SubscriptionId</span></span>
<span data-ttu-id="0eeeb-145">Specifica l'ID sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="0eeeb-145">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="0eeeb-146">-UserId</span><span class="sxs-lookup"><span data-stu-id="0eeeb-146">-UserId</span></span>
<span data-ttu-id="0eeeb-147">Il proprietario dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="0eeeb-147">The owner of the subscription.</span></span> <span data-ttu-id="0eeeb-148">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="0eeeb-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="0eeeb-149">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0eeeb-149">-Confirm</span></span>
<span data-ttu-id="0eeeb-150">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0eeeb-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0eeeb-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0eeeb-151">-WhatIf</span></span>
<span data-ttu-id="0eeeb-152">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0eeeb-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0eeeb-153">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0eeeb-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0eeeb-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eeeb-154">CommonParameters</span></span>
<span data-ttu-id="0eeeb-155">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0eeeb-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eeeb-156">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0eeeb-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eeeb-157">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0eeeb-157">INPUTS</span></span>

### <span data-ttu-id="0eeeb-158">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0eeeb-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0eeeb-159">System. String</span><span class="sxs-lookup"><span data-stu-id="0eeeb-159">System.String</span></span>

### <span data-ttu-id="0eeeb-160">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscriptionState, Microsoft. Azure. PowerShell. Cmdlets. ApiManagement. ServiceManagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="0eeeb-160">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="0eeeb-161">System. Nullable ' 1 [[System. DateTime, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0eeeb-161">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="0eeeb-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0eeeb-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0eeeb-163">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0eeeb-163">OUTPUTS</span></span>

### <span data-ttu-id="0eeeb-164">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="0eeeb-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="0eeeb-165">Note</span><span class="sxs-lookup"><span data-stu-id="0eeeb-165">NOTES</span></span>

## <span data-ttu-id="0eeeb-166">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0eeeb-166">RELATED LINKS</span></span>

[<span data-ttu-id="0eeeb-167">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="0eeeb-167">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="0eeeb-168">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="0eeeb-168">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="0eeeb-169">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="0eeeb-169">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)


