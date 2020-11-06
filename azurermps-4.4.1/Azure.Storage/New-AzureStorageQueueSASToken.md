---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 42C669B6-B621-454C-B897-262E1C8E76E3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueueSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueueSASToken.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 904305e383803e8ef672a82689794296f7c9b84d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93522017"
---
# <span data-ttu-id="5291a-101">New-AzureStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="5291a-101">New-AzureStorageQueueSASToken</span></span>

## <span data-ttu-id="5291a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5291a-102">SYNOPSIS</span></span>
<span data-ttu-id="5291a-103">Genera un token della firma di accesso condiviso per una coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="5291a-103">Generates a shared access signature token for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5291a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5291a-104">SYNTAX</span></span>

### <span data-ttu-id="5291a-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="5291a-105">SasPolicy</span></span>
```
New-AzureStorageQueueSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="5291a-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="5291a-106">SasPermission</span></span>
```
New-AzureStorageQueueSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="5291a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5291a-107">DESCRIPTION</span></span>
<span data-ttu-id="5291a-108">Il cmdlet **New-AzureStorageQueueSASToken** genera il token della firma di accesso condiviso per una coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="5291a-108">The **New-AzureStorageQueueSASToken** cmdlet generates shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="5291a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5291a-109">EXAMPLES</span></span>

### <span data-ttu-id="5291a-110">Esempio 1: generare un token SAS della coda con l'autorizzazione completa</span><span class="sxs-lookup"><span data-stu-id="5291a-110">Example 1: Generate a queue SAS token with full permission</span></span>
```
PS C:\>New-AzureStorageQueueSASToken -Name "Test" -Permission raup
```

<span data-ttu-id="5291a-111">Questo esempio genera un token SAS Queue con l'autorizzazione completa.</span><span class="sxs-lookup"><span data-stu-id="5291a-111">This example generates a queue SAS token with full permission.</span></span>

## <span data-ttu-id="5291a-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5291a-112">PARAMETERS</span></span>

### <span data-ttu-id="5291a-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="5291a-113">-Context</span></span>
<span data-ttu-id="5291a-114">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="5291a-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="5291a-115">Puoi crearla tramite il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="5291a-115">You can create it by New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5291a-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="5291a-116">-ExpiryTime</span></span>
<span data-ttu-id="5291a-117">Specifica quando la firma di accesso condiviso non è più valida.</span><span class="sxs-lookup"><span data-stu-id="5291a-117">Specifies when the shared access signature is no longer valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5291a-118">-FullUri</span><span class="sxs-lookup"><span data-stu-id="5291a-118">-FullUri</span></span>
<span data-ttu-id="5291a-119">Indica che questo cmdlet restituisce l'URI BLOB completo e il token della firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="5291a-119">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="5291a-120">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="5291a-120">-IPAddressOrRange</span></span>
<span data-ttu-id="5291a-121">Specifica l'indirizzo IP o l'intervallo di indirizzi IP da cui accettare le richieste, ad esempio 168.1.5.65 o 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="5291a-121">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="5291a-122">L'intervallo è incluso.</span><span class="sxs-lookup"><span data-stu-id="5291a-122">The range is inclusive.</span></span>

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

### <span data-ttu-id="5291a-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="5291a-123">-Name</span></span>
<span data-ttu-id="5291a-124">Specifica un nome di coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="5291a-124">Specifies an Azure storage queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5291a-125">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="5291a-125">-Permission</span></span>
<span data-ttu-id="5291a-126">Specifica le autorizzazioni per una coda di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="5291a-126">Specifies permissions for a storage queue.</span></span>

```yaml
Type: String
Parameter Sets: SasPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5291a-127">-Policy</span><span class="sxs-lookup"><span data-stu-id="5291a-127">-Policy</span></span>
<span data-ttu-id="5291a-128">Specifica un criterio di accesso archiviato in Azure.</span><span class="sxs-lookup"><span data-stu-id="5291a-128">Specifies an Azure stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: SasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5291a-129">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="5291a-129">-Protocol</span></span>
<span data-ttu-id="5291a-130">Specifica il protocollo consentito per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="5291a-130">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="5291a-131">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="5291a-131">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="5291a-132">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="5291a-132">HttpsOnly</span></span>
* <span data-ttu-id="5291a-133">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="5291a-133">HttpsOrHttp</span></span>

<span data-ttu-id="5291a-134">Il valore predefinito è HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="5291a-134">The default value is HttpsOrHttp.</span></span>

```yaml
Type: SharedAccessProtocol
Parameter Sets: (All)
Aliases: 
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5291a-135">-StartTime</span><span class="sxs-lookup"><span data-stu-id="5291a-135">-StartTime</span></span>
<span data-ttu-id="5291a-136">Specifica quando la firma di accesso condiviso diventa valida.</span><span class="sxs-lookup"><span data-stu-id="5291a-136">Specifies when the shared access signature becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5291a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5291a-137">CommonParameters</span></span>
<span data-ttu-id="5291a-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5291a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5291a-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5291a-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5291a-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5291a-140">INPUTS</span></span>

### <span data-ttu-id="5291a-141">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="5291a-141">IStorageContext</span></span>

<span data-ttu-id="5291a-142">Il parametro "context" accetta il valore di tipo "IStorageContext" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="5291a-142">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="5291a-143">Stringa</span><span class="sxs-lookup"><span data-stu-id="5291a-143">String</span></span>

<span data-ttu-id="5291a-144">Il parametro "Name" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="5291a-144">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="5291a-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5291a-145">OUTPUTS</span></span>

### <span data-ttu-id="5291a-146">System. String</span><span class="sxs-lookup"><span data-stu-id="5291a-146">System.String</span></span>

## <span data-ttu-id="5291a-147">Note</span><span class="sxs-lookup"><span data-stu-id="5291a-147">NOTES</span></span>

## <span data-ttu-id="5291a-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5291a-148">RELATED LINKS</span></span>

