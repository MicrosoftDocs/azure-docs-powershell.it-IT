---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
ms.openlocfilehash: c747d85f87e88c3f72ae86c8bcef771b3e42c91a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509411"
---
# <span data-ttu-id="54df5-101">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="54df5-101">Set-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="54df5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="54df5-102">SYNOPSIS</span></span>
<span data-ttu-id="54df5-103">Imposta i dettagli degli abbonamenti esistenti.</span><span class="sxs-lookup"><span data-stu-id="54df5-103">Sets existing subscription details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54df5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="54df5-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="54df5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="54df5-105">DESCRIPTION</span></span>
<span data-ttu-id="54df5-106">Il cmdlet **set-AzureRmApiManagementSubscription** imposta i dettagli di sottoscrizione esistenti.</span><span class="sxs-lookup"><span data-stu-id="54df5-106">The **Set-AzureRmApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="54df5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="54df5-107">EXAMPLES</span></span>

### <span data-ttu-id="54df5-108">Esempio 1: impostare lo stato e le chiavi primarie e secondarie per un abbonamento</span><span class="sxs-lookup"><span data-stu-id="54df5-108">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SecondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="54df5-109">Questo comando imposta le chiavi primarie e secondarie per un abbonamento e lo attiva.</span><span class="sxs-lookup"><span data-stu-id="54df5-109">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="54df5-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="54df5-110">PARAMETERS</span></span>

### <span data-ttu-id="54df5-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="54df5-111">-Context</span></span>
<span data-ttu-id="54df5-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="54df5-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="54df5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54df5-113">-DefaultProfile</span></span>
<span data-ttu-id="54df5-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="54df5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54df5-115">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="54df5-115">-ExpiresOn</span></span>
<span data-ttu-id="54df5-116">Specifica una data di scadenza dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="54df5-116">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="54df5-117">Il valore predefinito di questo parametro è $Null.</span><span class="sxs-lookup"><span data-stu-id="54df5-117">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="54df5-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="54df5-118">-Name</span></span>
<span data-ttu-id="54df5-119">Specifica un nome di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="54df5-119">Specifies a subscription name.</span></span>

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

### <span data-ttu-id="54df5-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="54df5-120">-PassThru</span></span>
<span data-ttu-id="54df5-121">PassThru</span><span class="sxs-lookup"><span data-stu-id="54df5-121">passthru</span></span>

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

### <span data-ttu-id="54df5-122">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="54df5-122">-PrimaryKey</span></span>
<span data-ttu-id="54df5-123">Specifica la chiave primaria dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="54df5-123">Specifies the subscription primary key.</span></span>
<span data-ttu-id="54df5-124">Questo parametro viene generato automaticamente se non specificato.</span><span class="sxs-lookup"><span data-stu-id="54df5-124">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="54df5-125">Questo parametro deve essere lungo da 1 a 300 caratteri.</span><span class="sxs-lookup"><span data-stu-id="54df5-125">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="54df5-126">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="54df5-126">-SecondaryKey</span></span>
<span data-ttu-id="54df5-127">Specifica la chiave secondaria dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="54df5-127">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="54df5-128">Questo parametro viene generato automaticamente se non specificato.</span><span class="sxs-lookup"><span data-stu-id="54df5-128">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="54df5-129">Questo parametro deve essere lungo da 1 a 300 caratteri.</span><span class="sxs-lookup"><span data-stu-id="54df5-129">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="54df5-130">-Stato</span><span class="sxs-lookup"><span data-stu-id="54df5-130">-State</span></span>
<span data-ttu-id="54df5-131">Specifica lo stato dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="54df5-131">Specifies the subscription state.</span></span>
<span data-ttu-id="54df5-132">Il valore predefinito di questo parametro è $Null.</span><span class="sxs-lookup"><span data-stu-id="54df5-132">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="54df5-133">-StateComment</span><span class="sxs-lookup"><span data-stu-id="54df5-133">-StateComment</span></span>
<span data-ttu-id="54df5-134">Specifica il commento sullo stato dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="54df5-134">Specifies the subscription state comment.</span></span>
<span data-ttu-id="54df5-135">Il valore predefinito di questo parametro è $Null.</span><span class="sxs-lookup"><span data-stu-id="54df5-135">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="54df5-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="54df5-136">-SubscriptionId</span></span>
<span data-ttu-id="54df5-137">Specifica l'ID sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="54df5-137">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="54df5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54df5-138">CommonParameters</span></span>
<span data-ttu-id="54df5-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54df5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54df5-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54df5-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54df5-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="54df5-141">INPUTS</span></span>

### <span data-ttu-id="54df5-142">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="54df5-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="54df5-143">System. String</span><span class="sxs-lookup"><span data-stu-id="54df5-143">System.String</span></span>

### <span data-ttu-id="54df5-144">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscriptionState, Microsoft. Azure. Commands. ApiManagement. ServiceManagement, Version = 6.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="54df5-144">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.Commands.ApiManagement.ServiceManagement, Version=6.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="54df5-145">System. Nullable ' 1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="54df5-145">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="54df5-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="54df5-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="54df5-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="54df5-147">OUTPUTS</span></span>

### <span data-ttu-id="54df5-148">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="54df5-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="54df5-149">Note</span><span class="sxs-lookup"><span data-stu-id="54df5-149">NOTES</span></span>

## <span data-ttu-id="54df5-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="54df5-150">RELATED LINKS</span></span>

[<span data-ttu-id="54df5-151">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="54df5-151">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="54df5-152">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="54df5-152">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="54df5-153">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="54df5-153">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)


