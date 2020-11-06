---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 3b6d07577a6df05a57ed7675f5d14c847e8c33fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510783"
---
# <span data-ttu-id="b6fbd-101">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="b6fbd-101">Set-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="b6fbd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b6fbd-102">SYNOPSIS</span></span>
<span data-ttu-id="b6fbd-103">Imposta i dettagli degli abbonamenti esistenti.</span><span class="sxs-lookup"><span data-stu-id="b6fbd-103">Sets existing subscription details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6fbd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b6fbd-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b6fbd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b6fbd-105">DESCRIPTION</span></span>
<span data-ttu-id="b6fbd-106">Il cmdlet **set-AzureRmApiManagementSubscription** imposta i dettagli di sottoscrizione esistenti.</span><span class="sxs-lookup"><span data-stu-id="b6fbd-106">The **Set-AzureRmApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="b6fbd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b6fbd-107">EXAMPLES</span></span>

### <span data-ttu-id="b6fbd-108">Esempio 1: impostare lo stato e le chiavi primarie e secondarie per un abbonamento</span><span class="sxs-lookup"><span data-stu-id="b6fbd-108">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```
PS C:\>Set-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SencondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="b6fbd-109">Questo comando imposta le chiavi primarie e secondarie per un abbonamento e lo attiva.</span><span class="sxs-lookup"><span data-stu-id="b6fbd-109">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="b6fbd-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b6fbd-110">PARAMETERS</span></span>

### <span data-ttu-id="b6fbd-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="b6fbd-111">-Context</span></span>
<span data-ttu-id="b6fbd-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="b6fbd-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b6fbd-113">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="b6fbd-113">-ExpiresOn</span></span>
<span data-ttu-id="b6fbd-114">Specifica una data di scadenza dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="b6fbd-114">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="b6fbd-115">Il valore predefinito di questo parametro è $Null.</span><span class="sxs-lookup"><span data-stu-id="b6fbd-115">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="b6fbd-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="b6fbd-116">-Name</span></span>
<span data-ttu-id="b6fbd-117">Specifica un nome di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="b6fbd-117">Specifies a subscription name.</span></span>

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

### <span data-ttu-id="b6fbd-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6fbd-118">-PassThru</span></span>
<span data-ttu-id="b6fbd-119">PassThru</span><span class="sxs-lookup"><span data-stu-id="b6fbd-119">passthru</span></span>

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

### <span data-ttu-id="b6fbd-120">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="b6fbd-120">-PrimaryKey</span></span>
<span data-ttu-id="b6fbd-121">Specifica la chiave primaria dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="b6fbd-121">Specifies the subscription primary key.</span></span>
<span data-ttu-id="b6fbd-122">Questo parametro viene generato automaticamente se non specificato.</span><span class="sxs-lookup"><span data-stu-id="b6fbd-122">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="b6fbd-123">Questo parametro deve essere lungo da 1 a 300 caratteri.</span><span class="sxs-lookup"><span data-stu-id="b6fbd-123">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="b6fbd-124">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="b6fbd-124">-SecondaryKey</span></span>
<span data-ttu-id="b6fbd-125">Specifica la chiave secondaria dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="b6fbd-125">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="b6fbd-126">Questo parametro viene generato automaticamente se non specificato.</span><span class="sxs-lookup"><span data-stu-id="b6fbd-126">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="b6fbd-127">Questo parametro deve essere lungo da 1 a 300 caratteri.</span><span class="sxs-lookup"><span data-stu-id="b6fbd-127">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="b6fbd-128">-Stato</span><span class="sxs-lookup"><span data-stu-id="b6fbd-128">-State</span></span>
<span data-ttu-id="b6fbd-129">Specifica lo stato dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="b6fbd-129">Specifies the subscription state.</span></span>
<span data-ttu-id="b6fbd-130">Il valore predefinito di questo parametro è $Null.</span><span class="sxs-lookup"><span data-stu-id="b6fbd-130">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="b6fbd-131">-StateComment</span><span class="sxs-lookup"><span data-stu-id="b6fbd-131">-StateComment</span></span>
<span data-ttu-id="b6fbd-132">Specifica il commento sullo stato dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="b6fbd-132">Specifies the subscription state comment.</span></span>
<span data-ttu-id="b6fbd-133">Il valore predefinito di questo parametro è $Null.</span><span class="sxs-lookup"><span data-stu-id="b6fbd-133">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="b6fbd-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b6fbd-134">-SubscriptionId</span></span>
<span data-ttu-id="b6fbd-135">Specifica l'ID sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="b6fbd-135">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="b6fbd-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6fbd-136">-DefaultProfile</span></span>
<span data-ttu-id="b6fbd-137">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b6fbd-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6fbd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6fbd-138">CommonParameters</span></span>
<span data-ttu-id="b6fbd-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6fbd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6fbd-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6fbd-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6fbd-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b6fbd-141">INPUTS</span></span>

## <span data-ttu-id="b6fbd-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b6fbd-142">OUTPUTS</span></span>

### <span data-ttu-id="b6fbd-143">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscripition</span><span class="sxs-lookup"><span data-stu-id="b6fbd-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscripition</span></span>

## <span data-ttu-id="b6fbd-144">Note</span><span class="sxs-lookup"><span data-stu-id="b6fbd-144">NOTES</span></span>

## <span data-ttu-id="b6fbd-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b6fbd-145">RELATED LINKS</span></span>

[<span data-ttu-id="b6fbd-146">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="b6fbd-146">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="b6fbd-147">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="b6fbd-147">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="b6fbd-148">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="b6fbd-148">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)


