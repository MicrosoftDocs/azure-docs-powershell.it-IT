---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContext.md
gitcommit: https://github.com/Azure/azure-powershell/blob/89262bc4144696c69376c3fb654c881de55b6450
ms.openlocfilehash: 2e9d3689a29a54f7af873cd1a11fdbc343509eb7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688541"
---
# <span data-ttu-id="d3fad-101">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="d3fad-101">New-AzureStorageContext</span></span>

## <span data-ttu-id="d3fad-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d3fad-102">SYNOPSIS</span></span>
<span data-ttu-id="d3fad-103">Crea un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d3fad-103">Creates an Azure Storage context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3fad-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d3fad-104">SYNTAX</span></span>

### <span data-ttu-id="d3fad-105">AccountNameAndKey (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d3fad-105">AccountNameAndKey (Default)</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="d3fad-106">AccountNameAndKeyEnvironment</span><span class="sxs-lookup"><span data-stu-id="d3fad-106">AccountNameAndKeyEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="d3fad-107">AnonymousAccount</span><span class="sxs-lookup"><span data-stu-id="d3fad-107">AnonymousAccount</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="d3fad-108">AnonymousAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="d3fad-108">AnonymousAccountEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="d3fad-109">SasToken</span><span class="sxs-lookup"><span data-stu-id="d3fad-109">SasToken</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="d3fad-110">SasTokenWithAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="d3fad-110">SasTokenWithAzureEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="d3fad-111">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="d3fad-111">ConnectionString</span></span>
```
New-AzureStorageContext -ConnectionString <String> [<CommonParameters>]
```

### <span data-ttu-id="d3fad-112">LocalDevelopment</span><span class="sxs-lookup"><span data-stu-id="d3fad-112">LocalDevelopment</span></span>
```
New-AzureStorageContext [-Local] [<CommonParameters>]
```

## <span data-ttu-id="d3fad-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3fad-113">DESCRIPTION</span></span>
<span data-ttu-id="d3fad-114">Il cmdlet **New-AzureStorageContext** crea un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d3fad-114">The **New-AzureStorageContext** cmdlet creates an Azure Storage context.</span></span>

## <span data-ttu-id="d3fad-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d3fad-115">EXAMPLES</span></span>

### <span data-ttu-id="d3fad-116">Esempio 1: creare un contesto specificando un nome e una chiave dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="d3fad-116">Example 1: Create a context by specifying a storage account name and key</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

<span data-ttu-id="d3fad-117">Questo comando crea un contesto per l'account denominato ContosoGeneral che usa la chiave specificata.</span><span class="sxs-lookup"><span data-stu-id="d3fad-117">This command creates a context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="d3fad-118">Esempio 2: creare un contesto specificando una stringa di connessione</span><span class="sxs-lookup"><span data-stu-id="d3fad-118">Example 2: Create a context by specifying a connection string</span></span>
```
C:\PS>New-AzureStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

<span data-ttu-id="d3fad-119">Questo comando crea un contesto basato sulla stringa di connessione specificata per l'account ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="d3fad-119">This command creates a context based on the specified connection string for the account ContosoGeneral.</span></span>

### <span data-ttu-id="d3fad-120">Esempio 3: creare un contesto per un account di archiviazione Anonimo</span><span class="sxs-lookup"><span data-stu-id="d3fad-120">Example 3: Create a context for an anonymous storage account</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

<span data-ttu-id="d3fad-121">Questo comando crea un contesto per l'uso anonimo per l'account denominato ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="d3fad-121">This command creates a context for anonymous use for the account named ContosoGeneral.</span></span>
<span data-ttu-id="d3fad-122">Il comando specifica HTTP come protocollo di connessione.</span><span class="sxs-lookup"><span data-stu-id="d3fad-122">The command specifies HTTP as a connection protocol.</span></span>

### <span data-ttu-id="d3fad-123">Esempio 4: creare un contesto usando l'account di archiviazione dello sviluppo locale</span><span class="sxs-lookup"><span data-stu-id="d3fad-123">Example 4: Create a context by using the local development storage account</span></span>
```
C:\PS>New-AzureStorageContext -Local
```

<span data-ttu-id="d3fad-124">Questo comando crea un contesto usando l'account di archiviazione dello sviluppo locale.</span><span class="sxs-lookup"><span data-stu-id="d3fad-124">This command creates a context by using the local development storage account.</span></span>
<span data-ttu-id="d3fad-125">Il comando specifica il parametro *local* .</span><span class="sxs-lookup"><span data-stu-id="d3fad-125">The command specifies the *Local* parameter.</span></span>

### <span data-ttu-id="d3fad-126">Esempio 5: ottenere il contenitore per l'account di archiviazione dello sviluppatore locale</span><span class="sxs-lookup"><span data-stu-id="d3fad-126">Example 5: Get the container for the local developer storage account</span></span>
```
C:\PS>New-AzureStorageContext -Local | Get-AzureStorageContainer
```

<span data-ttu-id="d3fad-127">Questo comando crea un contesto usando l'account di archiviazione dello sviluppo locale e quindi passa il nuovo contesto al cmdlet **Get-AzureStorageContainer** usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="d3fad-127">This command creates a context by using the local development storage account, and then passes the new context to the **Get-AzureStorageContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d3fad-128">Il comando ottiene il contenitore di archiviazione di Azure per l'account di archiviazione dello sviluppatore locale.</span><span class="sxs-lookup"><span data-stu-id="d3fad-128">The command gets the Azure Storage container for the local developer storage account.</span></span>

### <span data-ttu-id="d3fad-129">Esempio 6: ottenere più contenitori</span><span class="sxs-lookup"><span data-stu-id="d3fad-129">Example 6: Get multiple containers</span></span>
```
C:\PS>$Context01 = New-AzureStorageContext -Local 
PS C:\> $Context02 = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzureStorageContainer
```

<span data-ttu-id="d3fad-130">Con il primo comando viene creato un contesto utilizzando l'account di archiviazione dello sviluppo locale e il contesto viene archiviato nella variabile $Context 01.</span><span class="sxs-lookup"><span data-stu-id="d3fad-130">The first command creates a context by using the local development storage account, and then stores that context in the $Context01 variable.</span></span>

<span data-ttu-id="d3fad-131">Il secondo comando crea un contesto per l'account denominato ContosoGeneral che usa la chiave specificata e quindi archivia tale contesto nella variabile $Context 02.</span><span class="sxs-lookup"><span data-stu-id="d3fad-131">The second command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that context in the $Context02 variable.</span></span>

<span data-ttu-id="d3fad-132">Il comando finale recupera i contenitori per i contesti archiviati in $Context 01 e $Context 02 usando **Get-AzureStorageContainer**.</span><span class="sxs-lookup"><span data-stu-id="d3fad-132">The final command gets the containers for the contexts stored in $Context01 and $Context02 by using **Get-AzureStorageContainer**.</span></span>

### <span data-ttu-id="d3fad-133">Esempio 7: creare un contesto con un endpoint</span><span class="sxs-lookup"><span data-stu-id="d3fad-133">Example 7: Create a context with an endpoint</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

<span data-ttu-id="d3fad-134">Questo comando crea un contesto di archiviazione di Azure con l'endpoint di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="d3fad-134">This command creates an Azure Storage context that has the specified storage endpoint.</span></span>
<span data-ttu-id="d3fad-135">Il comando crea il contesto per l'account denominato ContosoGeneral che usa la chiave specificata.</span><span class="sxs-lookup"><span data-stu-id="d3fad-135">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="d3fad-136">Esempio 8: creare un contesto con un ambiente specificato</span><span class="sxs-lookup"><span data-stu-id="d3fad-136">Example 8: Create a context with a specified environment</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

<span data-ttu-id="d3fad-137">Questo comando crea un contesto di archiviazione di Azure con l'ambiente Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="d3fad-137">This command creates an Azure storage context that has the specified Azure environment.</span></span>
<span data-ttu-id="d3fad-138">Il comando crea il contesto per l'account denominato ContosoGeneral che usa la chiave specificata.</span><span class="sxs-lookup"><span data-stu-id="d3fad-138">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="d3fad-139">Esempio 9: creare un contesto usando un token SAS</span><span class="sxs-lookup"><span data-stu-id="d3fad-139">Example 9: Create a context by using an SAS token</span></span>
```
C:\PS>$SasToken = New-AzureStorageContainerSASToken -Name "ContosoMain" -Permission "raud"
PS C:\> $Context = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzureStorageBlob -Container "ContosoMain"
```

<span data-ttu-id="d3fad-140">Il primo comando genera un token SAS usando il cmdlet **New-AzureStorageContainerSASToken** per il contenitore denominato ContosoMain e quindi archivia tale token nella variabile $SasToken.</span><span class="sxs-lookup"><span data-stu-id="d3fad-140">The first command generates an SAS token by using the **New-AzureStorageContainerSASToken** cmdlet for the container named ContosoMain, and then stores that token in the $SasToken variable.</span></span>
<span data-ttu-id="d3fad-141">Il token è per le autorizzazioni di lettura, aggiunta, aggiornamento ed eliminazione.</span><span class="sxs-lookup"><span data-stu-id="d3fad-141">That token is for read, add, update, and delete permissions.</span></span>

<span data-ttu-id="d3fad-142">Il secondo comando crea un contesto per l'account denominato ContosoGeneral che usa il token SAS archiviato in $SasToken e quindi archivia tale contesto nella variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="d3fad-142">The second command creates a context for the account named ContosoGeneral that uses the SAS token stored in $SasToken, and then stores that context in the $Context variable.</span></span>

<span data-ttu-id="d3fad-143">Il comando finale elenca tutti i BLOB associati al contenitore denominato ContosoMain usando il contesto archiviato in $Context.</span><span class="sxs-lookup"><span data-stu-id="d3fad-143">The final command lists all the blobs associated with the container named ContosoMain by using the context stored in $Context.</span></span>

## <span data-ttu-id="d3fad-144">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d3fad-144">PARAMETERS</span></span>

### <span data-ttu-id="d3fad-145">-Anonimo</span><span class="sxs-lookup"><span data-stu-id="d3fad-145">-Anonymous</span></span>
<span data-ttu-id="d3fad-146">Indica che questo cmdlet crea un contesto di archiviazione di Azure per l'accesso anonimo.</span><span class="sxs-lookup"><span data-stu-id="d3fad-146">Indicates that this cmdlet creates an Azure Storage context for anonymous logon.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AnonymousAccount, AnonymousAccountEnvironment
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3fad-147">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="d3fad-147">-ConnectionString</span></span>
<span data-ttu-id="d3fad-148">Specifica una stringa di connessione per il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d3fad-148">Specifies a connection string for the Azure Storage context.</span></span>

```yaml
Type: String
Parameter Sets: ConnectionString
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3fad-149">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="d3fad-149">-Endpoint</span></span>
<span data-ttu-id="d3fad-150">Specifica l'endpoint per il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d3fad-150">Specifies the endpoint for the Azure Storage context.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameAndKey, AnonymousAccount, SasToken
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3fad-151">-Ambiente</span><span class="sxs-lookup"><span data-stu-id="d3fad-151">-Environment</span></span>
<span data-ttu-id="d3fad-152">Specifica l'ambiente Azure.</span><span class="sxs-lookup"><span data-stu-id="d3fad-152">Specifies the Azure environment.</span></span>
<span data-ttu-id="d3fad-153">I valori accettabili per questo parametro sono: AzureCloud e AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="d3fad-153">The acceptable values for this parameter are: AzureCloud and AzureChinaCloud.</span></span>
<span data-ttu-id="d3fad-154">Per altre informazioni, digitare `Get-Help Get-AzureEnvironment` .</span><span class="sxs-lookup"><span data-stu-id="d3fad-154">For more information, type `Get-Help Get-AzureEnvironment`.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameAndKeyEnvironment, AnonymousAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SasTokenWithAzureEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3fad-155">-Local</span><span class="sxs-lookup"><span data-stu-id="d3fad-155">-Local</span></span>
<span data-ttu-id="d3fad-156">Indica che questo cmdlet crea un contesto utilizzando l'account di archiviazione dello sviluppo locale.</span><span class="sxs-lookup"><span data-stu-id="d3fad-156">Indicates that this cmdlet creates a context by using the local development storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LocalDevelopment
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3fad-157">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="d3fad-157">-Protocol</span></span>
<span data-ttu-id="d3fad-158">Transfer Protocol (https/http).</span><span class="sxs-lookup"><span data-stu-id="d3fad-158">Transfer Protocol (https/http).</span></span>

```yaml
Type: String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken
Aliases: 
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3fad-159">-SasToken</span><span class="sxs-lookup"><span data-stu-id="d3fad-159">-SasToken</span></span>
<span data-ttu-id="d3fad-160">Specifica un token SAS (Shared Access Signature) per il contesto.</span><span class="sxs-lookup"><span data-stu-id="d3fad-160">Specifies a Shared Access Signature (SAS) token for the context.</span></span>

```yaml
Type: String
Parameter Sets: SasToken, SasTokenWithAzureEnvironment
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3fad-161">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d3fad-161">-StorageAccountKey</span></span>
<span data-ttu-id="d3fad-162">Specifica una chiave dell'account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d3fad-162">Specifies an Azure Storage account key.</span></span>
<span data-ttu-id="d3fad-163">Questo cmdlet crea un contesto per la chiave specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="d3fad-163">This cmdlet creates a context for the key that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3fad-164">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d3fad-164">-StorageAccountName</span></span>
<span data-ttu-id="d3fad-165">Specifica un nome dell'account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d3fad-165">Specifies an Azure Storage account name.</span></span>
<span data-ttu-id="d3fad-166">Questo cmdlet crea un contesto per l'account specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="d3fad-166">This cmdlet creates a context for the account that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, SasTokenWithAzureEnvironment
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3fad-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3fad-167">CommonParameters</span></span>
<span data-ttu-id="d3fad-168">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3fad-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3fad-169">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3fad-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3fad-170">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d3fad-170">INPUTS</span></span>

## <span data-ttu-id="d3fad-171">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3fad-171">OUTPUTS</span></span>

### <span data-ttu-id="d3fad-172">AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="d3fad-172">AzureStorageContext</span></span>

## <span data-ttu-id="d3fad-173">Note</span><span class="sxs-lookup"><span data-stu-id="d3fad-173">NOTES</span></span>

## <span data-ttu-id="d3fad-174">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d3fad-174">RELATED LINKS</span></span>

[<span data-ttu-id="d3fad-175">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="d3fad-175">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="d3fad-176">New-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="d3fad-176">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)


