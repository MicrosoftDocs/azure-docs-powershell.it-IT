---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
ms.openlocfilehash: cbdc876368f55ace6f77c04172dc2f0a53b0a7f6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93685128"
---
# <span data-ttu-id="4df2e-101">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="4df2e-101">Set-AzApiManagementSubscription</span></span>

## <span data-ttu-id="4df2e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4df2e-102">SYNOPSIS</span></span>
<span data-ttu-id="4df2e-103">Imposta i dettagli degli abbonamenti esistenti.</span><span class="sxs-lookup"><span data-stu-id="4df2e-103">Sets existing subscription details.</span></span>

## <span data-ttu-id="4df2e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4df2e-104">SYNTAX</span></span>

```
Set-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-Name <String>]
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4df2e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4df2e-105">DESCRIPTION</span></span>
<span data-ttu-id="4df2e-106">Il cmdlet **set-AzApiManagementSubscription** imposta i dettagli di sottoscrizione esistenti.</span><span class="sxs-lookup"><span data-stu-id="4df2e-106">The **Set-AzApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="4df2e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4df2e-107">EXAMPLES</span></span>

### <span data-ttu-id="4df2e-108">Esempio 1: impostare lo stato e le chiavi primarie e secondarie per un abbonamento</span><span class="sxs-lookup"><span data-stu-id="4df2e-108">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SecondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="4df2e-109">Questo comando imposta le chiavi primarie e secondarie per un abbonamento e lo attiva.</span><span class="sxs-lookup"><span data-stu-id="4df2e-109">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="4df2e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4df2e-110">PARAMETERS</span></span>

### <span data-ttu-id="4df2e-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="4df2e-111">-Context</span></span>
<span data-ttu-id="4df2e-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="4df2e-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4df2e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4df2e-113">-DefaultProfile</span></span>
<span data-ttu-id="4df2e-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4df2e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4df2e-115">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="4df2e-115">-ExpiresOn</span></span>
<span data-ttu-id="4df2e-116">Specifica una data di scadenza dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4df2e-116">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="4df2e-117">Il valore predefinito di questo parametro è $Null.</span><span class="sxs-lookup"><span data-stu-id="4df2e-117">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="4df2e-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="4df2e-118">-Name</span></span>
<span data-ttu-id="4df2e-119">Specifica un nome di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4df2e-119">Specifies a subscription name.</span></span>

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

### <span data-ttu-id="4df2e-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4df2e-120">-PassThru</span></span>
<span data-ttu-id="4df2e-121">PassThru</span><span class="sxs-lookup"><span data-stu-id="4df2e-121">passthru</span></span>

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

### <span data-ttu-id="4df2e-122">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="4df2e-122">-PrimaryKey</span></span>
<span data-ttu-id="4df2e-123">Specifica la chiave primaria dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4df2e-123">Specifies the subscription primary key.</span></span>
<span data-ttu-id="4df2e-124">Questo parametro viene generato automaticamente se non specificato.</span><span class="sxs-lookup"><span data-stu-id="4df2e-124">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="4df2e-125">Questo parametro deve essere lungo da 1 a 300 caratteri.</span><span class="sxs-lookup"><span data-stu-id="4df2e-125">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="4df2e-126">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="4df2e-126">-SecondaryKey</span></span>
<span data-ttu-id="4df2e-127">Specifica la chiave secondaria dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4df2e-127">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="4df2e-128">Questo parametro viene generato automaticamente se non specificato.</span><span class="sxs-lookup"><span data-stu-id="4df2e-128">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="4df2e-129">Questo parametro deve essere lungo da 1 a 300 caratteri.</span><span class="sxs-lookup"><span data-stu-id="4df2e-129">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="4df2e-130">-Stato</span><span class="sxs-lookup"><span data-stu-id="4df2e-130">-State</span></span>
<span data-ttu-id="4df2e-131">Specifica lo stato dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4df2e-131">Specifies the subscription state.</span></span>
<span data-ttu-id="4df2e-132">Il valore predefinito di questo parametro è $Null.</span><span class="sxs-lookup"><span data-stu-id="4df2e-132">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="4df2e-133">-StateComment</span><span class="sxs-lookup"><span data-stu-id="4df2e-133">-StateComment</span></span>
<span data-ttu-id="4df2e-134">Specifica il commento sullo stato dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4df2e-134">Specifies the subscription state comment.</span></span>
<span data-ttu-id="4df2e-135">Il valore predefinito di questo parametro è $Null.</span><span class="sxs-lookup"><span data-stu-id="4df2e-135">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="4df2e-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4df2e-136">-SubscriptionId</span></span>
<span data-ttu-id="4df2e-137">Specifica l'ID sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="4df2e-137">Specifies the subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4df2e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4df2e-138">CommonParameters</span></span>
<span data-ttu-id="4df2e-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4df2e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4df2e-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4df2e-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4df2e-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4df2e-141">INPUTS</span></span>

### <span data-ttu-id="4df2e-142">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4df2e-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4df2e-143">System. String</span><span class="sxs-lookup"><span data-stu-id="4df2e-143">System.String</span></span>

### <span data-ttu-id="4df2e-144">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscriptionState, Microsoft. Azure. PowerShell. Cmdlets. ApiManagement. ServiceManagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4df2e-144">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="4df2e-145">System. Nullable ' 1 [[System. DateTime, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4df2e-145">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4df2e-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4df2e-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4df2e-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4df2e-147">OUTPUTS</span></span>

### <span data-ttu-id="4df2e-148">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="4df2e-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="4df2e-149">Note</span><span class="sxs-lookup"><span data-stu-id="4df2e-149">NOTES</span></span>

## <span data-ttu-id="4df2e-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4df2e-150">RELATED LINKS</span></span>

[<span data-ttu-id="4df2e-151">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="4df2e-151">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="4df2e-152">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="4df2e-152">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="4df2e-153">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="4df2e-153">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)


