---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6FF04E82-4921-4F7B-83D0-6997316BC5FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainersastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
ms.openlocfilehash: 88b9d395cca2e548e3c70d55267b7c1b3854a750
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676577"
---
# <span data-ttu-id="3b59b-101">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="3b59b-101">New-AzStorageContainerSASToken</span></span>

## <span data-ttu-id="3b59b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3b59b-102">SYNOPSIS</span></span>
<span data-ttu-id="3b59b-103">Genera un token SAS per un contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3b59b-103">Generates an SAS token for an Azure storage container.</span></span>

## <span data-ttu-id="3b59b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3b59b-104">SYNTAX</span></span>

### <span data-ttu-id="3b59b-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="3b59b-105">SasPolicy</span></span>
```
New-AzStorageContainerSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b59b-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="3b59b-106">SasPermission</span></span>
```
New-AzStorageContainerSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b59b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3b59b-107">DESCRIPTION</span></span>
<span data-ttu-id="3b59b-108">Il cmdlet **New-AzStorageContainerSASToken** genera un token SAS (Shared Access Signature) per un contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3b59b-108">The **New-AzStorageContainerSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage container.</span></span>

## <span data-ttu-id="3b59b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3b59b-109">EXAMPLES</span></span>

### <span data-ttu-id="3b59b-110">Esempio 1: generare un token SAS contenitore con l'autorizzazione contenitore completo</span><span class="sxs-lookup"><span data-stu-id="3b59b-110">Example 1: Generate a container SAS token with full container permission</span></span>
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Permission rwdl
```

<span data-ttu-id="3b59b-111">Questo esempio genera un token SAS contenitore con l'autorizzazione contenitore completo.</span><span class="sxs-lookup"><span data-stu-id="3b59b-111">This example generates a container SAS token with full container permission.</span></span>

### <span data-ttu-id="3b59b-112">Esempio 2: generare più token SAS contenitore tramite pipeline</span><span class="sxs-lookup"><span data-stu-id="3b59b-112">Example 2: Generate multiple container SAS token by pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container test* | New-AzStorageContainerSASToken -Permission rwdl
```

<span data-ttu-id="3b59b-113">Questo esempio genera più token SAS contenitore usando la pipeline.</span><span class="sxs-lookup"><span data-stu-id="3b59b-113">This example generates multiple container SAS tokens by using the pipeline.</span></span>

### <span data-ttu-id="3b59b-114">Esempio 3: generare il token SAS contenitore con i criteri di accesso condiviso</span><span class="sxs-lookup"><span data-stu-id="3b59b-114">Example 3: Generate container SAS token with shared access policy</span></span>
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Policy "PolicyName"
```

<span data-ttu-id="3b59b-115">Questo esempio genera un token SAS contenitore con criteri di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="3b59b-115">This example generates a container SAS token with shared access policy.</span></span>

## <span data-ttu-id="3b59b-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3b59b-116">PARAMETERS</span></span>

### <span data-ttu-id="3b59b-117">-Contesto</span><span class="sxs-lookup"><span data-stu-id="3b59b-117">-Context</span></span>
<span data-ttu-id="3b59b-118">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3b59b-118">Specifies an Azure storage context.</span></span>
<span data-ttu-id="3b59b-119">Puoi crearlo usando il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="3b59b-119">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="3b59b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b59b-120">-DefaultProfile</span></span>
<span data-ttu-id="3b59b-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3b59b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b59b-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="3b59b-122">-ExpiryTime</span></span>
<span data-ttu-id="3b59b-123">Specifica il momento in cui la firma di accesso condiviso diventa non valida.</span><span class="sxs-lookup"><span data-stu-id="3b59b-123">Specifies the time at which the shared access signature becomes invalid.</span></span>
<span data-ttu-id="3b59b-124">Se l'utente imposta l'ora di inizio ma non quella di scadenza, l'ora di scadenza viene impostata sull'ora di inizio più un'ora.</span><span class="sxs-lookup"><span data-stu-id="3b59b-124">If the user sets the start time but not the expiry time, the expiry time is set to the start time plus one hour.</span></span>
<span data-ttu-id="3b59b-125">Se non viene specificato né l'ora di inizio né l'ora di scadenza, il tempo di scadenza viene impostato sull'ora corrente e su un orario.</span><span class="sxs-lookup"><span data-stu-id="3b59b-125">If neither the start time nor the expiry time is specified, the expiry time is set to the current time plus one hour.</span></span>

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

### <span data-ttu-id="3b59b-126">-FullUri</span><span class="sxs-lookup"><span data-stu-id="3b59b-126">-FullUri</span></span>
<span data-ttu-id="3b59b-127">Indica che questo cmdlet restituisce l'URI BLOB completo e il token della firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="3b59b-127">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="3b59b-128">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="3b59b-128">-IPAddressOrRange</span></span>
<span data-ttu-id="3b59b-129">Specifica l'indirizzo IP o l'intervallo di indirizzi IP da cui accettare le richieste, ad esempio 168.1.5.65 o 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="3b59b-129">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="3b59b-130">L'intervallo è incluso.</span><span class="sxs-lookup"><span data-stu-id="3b59b-130">The range is inclusive.</span></span>

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

### <span data-ttu-id="3b59b-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="3b59b-131">-Name</span></span>
<span data-ttu-id="3b59b-132">Specifica un nome di contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3b59b-132">Specifies an Azure storage container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b59b-133">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="3b59b-133">-Permission</span></span>
<span data-ttu-id="3b59b-134">Specifica le autorizzazioni per un contenitore di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3b59b-134">Specifies permissions for a storage container.</span></span>
<span data-ttu-id="3b59b-135">È importante notare che si tratta di una stringa, ad esempio `rwd` (per lettura, scrittura ed eliminazione).</span><span class="sxs-lookup"><span data-stu-id="3b59b-135">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="3b59b-136">-Policy</span><span class="sxs-lookup"><span data-stu-id="3b59b-136">-Policy</span></span>
<span data-ttu-id="3b59b-137">Specifica un criterio di accesso archiviato in Azure.</span><span class="sxs-lookup"><span data-stu-id="3b59b-137">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="3b59b-138">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="3b59b-138">-Protocol</span></span>
<span data-ttu-id="3b59b-139">Specifica il protocollo consentito per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="3b59b-139">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="3b59b-140">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="3b59b-140">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="3b59b-141">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="3b59b-141">HttpsOnly</span></span>
* <span data-ttu-id="3b59b-142">HttpsOrHttp il valore predefinito è HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="3b59b-142">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="3b59b-143">-StartTime</span><span class="sxs-lookup"><span data-stu-id="3b59b-143">-StartTime</span></span>
<span data-ttu-id="3b59b-144">Specifica il momento in cui la firma di accesso condiviso diventa valida.</span><span class="sxs-lookup"><span data-stu-id="3b59b-144">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="3b59b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b59b-145">CommonParameters</span></span>
<span data-ttu-id="3b59b-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b59b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b59b-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b59b-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b59b-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3b59b-148">INPUTS</span></span>

### <span data-ttu-id="3b59b-149">System. String</span><span class="sxs-lookup"><span data-stu-id="3b59b-149">System.String</span></span>

### <span data-ttu-id="3b59b-150">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3b59b-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3b59b-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3b59b-151">OUTPUTS</span></span>

### <span data-ttu-id="3b59b-152">System. String</span><span class="sxs-lookup"><span data-stu-id="3b59b-152">System.String</span></span>

## <span data-ttu-id="3b59b-153">Note</span><span class="sxs-lookup"><span data-stu-id="3b59b-153">NOTES</span></span>

## <span data-ttu-id="3b59b-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3b59b-154">RELATED LINKS</span></span>

[<span data-ttu-id="3b59b-155">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="3b59b-155">New-AzStorageBlobSASToken</span></span>](./New-AzStorageBlobSASToken.md)