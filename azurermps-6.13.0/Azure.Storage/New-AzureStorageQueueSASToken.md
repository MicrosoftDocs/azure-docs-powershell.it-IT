---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 42C669B6-B621-454C-B897-262E1C8E76E3
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragequeuesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueueSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueueSASToken.md
ms.openlocfilehash: 337dcb1718cf48488115e38052c0fdfed73edc3e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517772"
---
# <span data-ttu-id="3e755-101">New-AzureStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="3e755-101">New-AzureStorageQueueSASToken</span></span>

## <span data-ttu-id="3e755-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3e755-102">SYNOPSIS</span></span>
<span data-ttu-id="3e755-103">Genera un token della firma di accesso condiviso per una coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3e755-103">Generates a shared access signature token for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e755-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3e755-104">SYNTAX</span></span>

### <span data-ttu-id="3e755-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="3e755-105">SasPolicy</span></span>
```
New-AzureStorageQueueSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e755-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="3e755-106">SasPermission</span></span>
```
New-AzureStorageQueueSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e755-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e755-107">DESCRIPTION</span></span>
<span data-ttu-id="3e755-108">Il cmdlet **New-AzureStorageQueueSASToken** genera il token della firma di accesso condiviso per una coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3e755-108">The **New-AzureStorageQueueSASToken** cmdlet generates shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="3e755-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3e755-109">EXAMPLES</span></span>

### <span data-ttu-id="3e755-110">Esempio 1: generare un token SAS della coda con l'autorizzazione completa</span><span class="sxs-lookup"><span data-stu-id="3e755-110">Example 1: Generate a queue SAS token with full permission</span></span>
```
PS C:\>New-AzureStorageQueueSASToken -Name "Test" -Permission raup
```

<span data-ttu-id="3e755-111">Questo esempio genera un token SAS Queue con l'autorizzazione completa.</span><span class="sxs-lookup"><span data-stu-id="3e755-111">This example generates a queue SAS token with full permission.</span></span>

## <span data-ttu-id="3e755-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3e755-112">PARAMETERS</span></span>

### <span data-ttu-id="3e755-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="3e755-113">-Context</span></span>
<span data-ttu-id="3e755-114">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3e755-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="3e755-115">Puoi crearla tramite il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="3e755-115">You can create it by New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e755-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e755-116">-DefaultProfile</span></span>
<span data-ttu-id="3e755-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3e755-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e755-118">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="3e755-118">-ExpiryTime</span></span>
<span data-ttu-id="3e755-119">Specifica quando la firma di accesso condiviso non è più valida.</span><span class="sxs-lookup"><span data-stu-id="3e755-119">Specifies when the shared access signature is no longer valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e755-120">-FullUri</span><span class="sxs-lookup"><span data-stu-id="3e755-120">-FullUri</span></span>
<span data-ttu-id="3e755-121">Indica che questo cmdlet restituisce l'URI BLOB completo e il token della firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="3e755-121">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="3e755-122">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="3e755-122">-IPAddressOrRange</span></span>
<span data-ttu-id="3e755-123">Specifica l'indirizzo IP o l'intervallo di indirizzi IP da cui accettare le richieste, ad esempio 168.1.5.65 o 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="3e755-123">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="3e755-124">L'intervallo è incluso.</span><span class="sxs-lookup"><span data-stu-id="3e755-124">The range is inclusive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e755-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="3e755-125">-Name</span></span>
<span data-ttu-id="3e755-126">Specifica un nome di coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3e755-126">Specifies an Azure storage queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e755-127">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="3e755-127">-Permission</span></span>
<span data-ttu-id="3e755-128">Specifica le autorizzazioni per una coda di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3e755-128">Specifies permissions for a storage queue.</span></span>
<span data-ttu-id="3e755-129">È importante notare che si tratta di una stringa, ad esempio `rwd` (per lettura, scrittura ed eliminazione).</span><span class="sxs-lookup"><span data-stu-id="3e755-129">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: SasPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e755-130">-Policy</span><span class="sxs-lookup"><span data-stu-id="3e755-130">-Policy</span></span>
<span data-ttu-id="3e755-131">Specifica un criterio di accesso archiviato in Azure.</span><span class="sxs-lookup"><span data-stu-id="3e755-131">Specifies an Azure stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: SasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e755-132">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="3e755-132">-Protocol</span></span>
<span data-ttu-id="3e755-133">Specifica il protocollo consentito per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="3e755-133">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="3e755-134">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="3e755-134">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="3e755-135">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="3e755-135">HttpsOnly</span></span>
* <span data-ttu-id="3e755-136">HttpsOrHttp il valore predefinito è HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="3e755-136">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAzure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e755-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="3e755-137">-StartTime</span></span>
<span data-ttu-id="3e755-138">Specifica quando la firma di accesso condiviso diventa valida.</span><span class="sxs-lookup"><span data-stu-id="3e755-138">Specifies when the shared access signature becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e755-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e755-139">CommonParameters</span></span>
<span data-ttu-id="3e755-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e755-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e755-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e755-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e755-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3e755-142">INPUTS</span></span>

### <span data-ttu-id="3e755-143">System. String</span><span class="sxs-lookup"><span data-stu-id="3e755-143">System.String</span></span>

### <span data-ttu-id="3e755-144">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3e755-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3e755-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3e755-145">OUTPUTS</span></span>

### <span data-ttu-id="3e755-146">System. String</span><span class="sxs-lookup"><span data-stu-id="3e755-146">System.String</span></span>

## <span data-ttu-id="3e755-147">Note</span><span class="sxs-lookup"><span data-stu-id="3e755-147">NOTES</span></span>

## <span data-ttu-id="3e755-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3e755-148">RELATED LINKS</span></span>
