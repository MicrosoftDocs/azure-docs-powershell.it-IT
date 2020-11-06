---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 62c1bd394dd509b81a8ea748c26c0465718926c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520723"
---
# <span data-ttu-id="4ec21-101">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="4ec21-101">Set-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="4ec21-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4ec21-102">SYNOPSIS</span></span>
<span data-ttu-id="4ec21-103">Imposta i dettagli degli abbonamenti esistenti.</span><span class="sxs-lookup"><span data-stu-id="4ec21-103">Sets existing subscription details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ec21-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4ec21-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4ec21-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4ec21-105">DESCRIPTION</span></span>
<span data-ttu-id="4ec21-106">Il cmdlet **set-AzureRmApiManagementSubscription** imposta i dettagli di sottoscrizione esistenti.</span><span class="sxs-lookup"><span data-stu-id="4ec21-106">The **Set-AzureRmApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="4ec21-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4ec21-107">EXAMPLES</span></span>

### <span data-ttu-id="4ec21-108">Esempio 1: impostare lo stato e le chiavi primarie e secondarie per un abbonamento</span><span class="sxs-lookup"><span data-stu-id="4ec21-108">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SecondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="4ec21-109">Questo comando imposta le chiavi primarie e secondarie per un abbonamento e lo attiva.</span><span class="sxs-lookup"><span data-stu-id="4ec21-109">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="4ec21-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4ec21-110">PARAMETERS</span></span>

### <span data-ttu-id="4ec21-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="4ec21-111">-Context</span></span>
<span data-ttu-id="4ec21-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="4ec21-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ec21-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ec21-113">-DefaultProfile</span></span>
<span data-ttu-id="4ec21-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4ec21-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="4ec21-115">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="4ec21-115">-ExpiresOn</span></span>
<span data-ttu-id="4ec21-116">Specifica una data di scadenza dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4ec21-116">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="4ec21-117">Il valore predefinito di questo parametro è $Null.</span><span class="sxs-lookup"><span data-stu-id="4ec21-117">The default value of this parameter is $Null.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ec21-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="4ec21-118">-Name</span></span>
<span data-ttu-id="4ec21-119">Specifica un nome di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4ec21-119">Specifies a subscription name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ec21-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4ec21-120">-PassThru</span></span>
<span data-ttu-id="4ec21-121">PassThru</span><span class="sxs-lookup"><span data-stu-id="4ec21-121">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ec21-122">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="4ec21-122">-PrimaryKey</span></span>
<span data-ttu-id="4ec21-123">Specifica la chiave primaria dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4ec21-123">Specifies the subscription primary key.</span></span>
<span data-ttu-id="4ec21-124">Questo parametro viene generato automaticamente se non specificato.</span><span class="sxs-lookup"><span data-stu-id="4ec21-124">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="4ec21-125">Questo parametro deve essere lungo da 1 a 300 caratteri.</span><span class="sxs-lookup"><span data-stu-id="4ec21-125">This parameter must be 1 to 300 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ec21-126">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="4ec21-126">-SecondaryKey</span></span>
<span data-ttu-id="4ec21-127">Specifica la chiave secondaria dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4ec21-127">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="4ec21-128">Questo parametro viene generato automaticamente se non specificato.</span><span class="sxs-lookup"><span data-stu-id="4ec21-128">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="4ec21-129">Questo parametro deve essere lungo da 1 a 300 caratteri.</span><span class="sxs-lookup"><span data-stu-id="4ec21-129">This parameter must be 1 to 300 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ec21-130">-Stato</span><span class="sxs-lookup"><span data-stu-id="4ec21-130">-State</span></span>
<span data-ttu-id="4ec21-131">Specifica lo stato dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4ec21-131">Specifies the subscription state.</span></span>
<span data-ttu-id="4ec21-132">Il valore predefinito di questo parametro è $Null.</span><span class="sxs-lookup"><span data-stu-id="4ec21-132">The default value of this parameter is $Null.</span></span>

```yaml
Type: PsApiManagementSubscriptionState
Parameter Sets: (All)
Aliases: 
Accepted values: Suspended, Active, Expired, Submitted, Rejected, Cancelled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ec21-133">-StateComment</span><span class="sxs-lookup"><span data-stu-id="4ec21-133">-StateComment</span></span>
<span data-ttu-id="4ec21-134">Specifica il commento sullo stato dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4ec21-134">Specifies the subscription state comment.</span></span>
<span data-ttu-id="4ec21-135">Il valore predefinito di questo parametro è $Null.</span><span class="sxs-lookup"><span data-stu-id="4ec21-135">The default value of this parameter is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ec21-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4ec21-136">-SubscriptionId</span></span>
<span data-ttu-id="4ec21-137">Specifica l'ID sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="4ec21-137">Specifies the subscription ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ec21-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ec21-138">CommonParameters</span></span>
<span data-ttu-id="4ec21-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ec21-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ec21-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ec21-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ec21-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4ec21-141">INPUTS</span></span>

### <span data-ttu-id="4ec21-142">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4ec21-142">None</span></span>
<span data-ttu-id="4ec21-143">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="4ec21-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4ec21-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4ec21-144">OUTPUTS</span></span>

### <span data-ttu-id="4ec21-145">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscripition</span><span class="sxs-lookup"><span data-stu-id="4ec21-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscripition</span></span>

## <span data-ttu-id="4ec21-146">Note</span><span class="sxs-lookup"><span data-stu-id="4ec21-146">NOTES</span></span>

## <span data-ttu-id="4ec21-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4ec21-147">RELATED LINKS</span></span>

[<span data-ttu-id="4ec21-148">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="4ec21-148">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="4ec21-149">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="4ec21-149">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="4ec21-150">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="4ec21-150">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)


