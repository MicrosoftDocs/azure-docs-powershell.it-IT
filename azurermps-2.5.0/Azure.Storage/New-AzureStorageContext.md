---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragecontext
schema: 2.0.0
ms.openlocfilehash: 3a91c88fe80151ef8aa3934c484cfe9b6671a750
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866598"
---
# <span data-ttu-id="d930c-101">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="d930c-101">New-AzureStorageContext</span></span>

## <span data-ttu-id="d930c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d930c-102">SYNOPSIS</span></span>
<span data-ttu-id="d930c-103">Crea un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d930c-103">Creates an Azure Storage context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d930c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d930c-104">SYNTAX</span></span>

### <span data-ttu-id="d930c-105">AccountNameAndKey (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d930c-105">AccountNameAndKey (Default)</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="d930c-106">AccountNameAndKeyEnvironment</span><span class="sxs-lookup"><span data-stu-id="d930c-106">AccountNameAndKeyEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="d930c-107">AnonymousAccount</span><span class="sxs-lookup"><span data-stu-id="d930c-107">AnonymousAccount</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="d930c-108">AnonymousAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="d930c-108">AnonymousAccountEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="d930c-109">SasToken</span><span class="sxs-lookup"><span data-stu-id="d930c-109">SasToken</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="d930c-110">SasTokenWithAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="d930c-110">SasTokenWithAzureEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="d930c-111">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="d930c-111">ConnectionString</span></span>
```
New-AzureStorageContext -ConnectionString <String> [<CommonParameters>]
```

### <span data-ttu-id="d930c-112">LocalDevelopment</span><span class="sxs-lookup"><span data-stu-id="d930c-112">LocalDevelopment</span></span>
```
New-AzureStorageContext [-Local] [<CommonParameters>]
```

## <span data-ttu-id="d930c-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d930c-113">DESCRIPTION</span></span>
<span data-ttu-id="d930c-114">Il cmdlet **New-AzureStorageContext** crea un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d930c-114">The **New-AzureStorageContext** cmdlet creates an Azure Storage context.</span></span>

## <span data-ttu-id="d930c-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d930c-115">EXAMPLES</span></span>

### <span data-ttu-id="d930c-116">Esempio 1: creare un contesto specificando un nome e una chiave dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="d930c-116">Example 1: Create a context by specifying a storage account name and key</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

<span data-ttu-id="d930c-117">Questo comando crea un contesto per l'account denominato ContosoGeneral che usa la chiave specificata.</span><span class="sxs-lookup"><span data-stu-id="d930c-117">This command creates a context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="d930c-118">Esempio 2: creare un contesto specificando una stringa di connessione</span><span class="sxs-lookup"><span data-stu-id="d930c-118">Example 2: Create a context by specifying a connection string</span></span>
```
C:\PS>New-AzureStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

<span data-ttu-id="d930c-119">Questo comando crea un contesto basato sulla stringa di connessione specificata per l'account ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="d930c-119">This command creates a context based on the specified connection string for the account ContosoGeneral.</span></span>

### <span data-ttu-id="d930c-120">Esempio 3: creare un contesto per un account di archiviazione Anonimo</span><span class="sxs-lookup"><span data-stu-id="d930c-120">Example 3: Create a context for an anonymous storage account</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

<span data-ttu-id="d930c-121">Questo comando crea un contesto per l'uso anonimo per l'account denominato ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="d930c-121">This command creates a context for anonymous use for the account named ContosoGeneral.</span></span>
<span data-ttu-id="d930c-122">Il comando specifica HTTP come protocollo di connessione.</span><span class="sxs-lookup"><span data-stu-id="d930c-122">The command specifies HTTP as a connection protocol.</span></span>

### <span data-ttu-id="d930c-123">Esempio 4: creare un contesto usando l'account di archiviazione dello sviluppo locale</span><span class="sxs-lookup"><span data-stu-id="d930c-123">Example 4: Create a context by using the local development storage account</span></span>
```
C:\PS>New-AzureStorageContext -Local
```

<span data-ttu-id="d930c-124">Questo comando crea un contesto usando l'account di archiviazione dello sviluppo locale.</span><span class="sxs-lookup"><span data-stu-id="d930c-124">This command creates a context by using the local development storage account.</span></span>
<span data-ttu-id="d930c-125">Il comando specifica il parametro *local* .</span><span class="sxs-lookup"><span data-stu-id="d930c-125">The command specifies the *Local* parameter.</span></span>

### <span data-ttu-id="d930c-126">Esempio 5: ottenere il contenitore per l'account di archiviazione dello sviluppatore locale</span><span class="sxs-lookup"><span data-stu-id="d930c-126">Example 5: Get the container for the local developer storage account</span></span>
```
C:\PS>New-AzureStorageContext -Local | Get-AzureStorageContainer
```

<span data-ttu-id="d930c-127">Questo comando crea un contesto usando l'account di archiviazione dello sviluppo locale e quindi passa il nuovo contesto al cmdlet **Get-AzureStorageContainer** usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="d930c-127">This command creates a context by using the local development storage account, and then passes the new context to the **Get-AzureStorageContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d930c-128">Il comando ottiene il contenitore di archiviazione di Azure per l'account di archiviazione dello sviluppatore locale.</span><span class="sxs-lookup"><span data-stu-id="d930c-128">The command gets the Azure Storage container for the local developer storage account.</span></span>

### <span data-ttu-id="d930c-129">Esempio 6: ottenere più contenitori</span><span class="sxs-lookup"><span data-stu-id="d930c-129">Example 6: Get multiple containers</span></span>
```
C:\PS>$Context01 = New-AzureStorageContext -Local 
PS C:\> $Context02 = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzureStorageContainer
```

<span data-ttu-id="d930c-130">Con il primo comando viene creato un contesto utilizzando l'account di archiviazione dello sviluppo locale e il contesto viene archiviato nella variabile $Context 01.</span><span class="sxs-lookup"><span data-stu-id="d930c-130">The first command creates a context by using the local development storage account, and then stores that context in the $Context01 variable.</span></span>
<span data-ttu-id="d930c-131">Il secondo comando crea un contesto per l'account denominato ContosoGeneral che usa la chiave specificata e quindi archivia tale contesto nella variabile $Context 02.</span><span class="sxs-lookup"><span data-stu-id="d930c-131">The second command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that context in the $Context02 variable.</span></span>
<span data-ttu-id="d930c-132">Il comando finale recupera i contenitori per i contesti archiviati in $Context 01 e $Context 02 usando **Get-AzureStorageContainer**.</span><span class="sxs-lookup"><span data-stu-id="d930c-132">The final command gets the containers for the contexts stored in $Context01 and $Context02 by using **Get-AzureStorageContainer**.</span></span>

### <span data-ttu-id="d930c-133">Esempio 7: creare un contesto con un endpoint</span><span class="sxs-lookup"><span data-stu-id="d930c-133">Example 7: Create a context with an endpoint</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

<span data-ttu-id="d930c-134">Questo comando crea un contesto di archiviazione di Azure con l'endpoint di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="d930c-134">This command creates an Azure Storage context that has the specified storage endpoint.</span></span>
<span data-ttu-id="d930c-135">Il comando crea il contesto per l'account denominato ContosoGeneral che usa la chiave specificata.</span><span class="sxs-lookup"><span data-stu-id="d930c-135">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="d930c-136">Esempio 8: creare un contesto con un ambiente specificato</span><span class="sxs-lookup"><span data-stu-id="d930c-136">Example 8: Create a context with a specified environment</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

<span data-ttu-id="d930c-137">Questo comando crea un contesto di archiviazione di Azure con l'ambiente Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="d930c-137">This command creates an Azure storage context that has the specified Azure environment.</span></span>
<span data-ttu-id="d930c-138">Il comando crea il contesto per l'account denominato ContosoGeneral che usa la chiave specificata.</span><span class="sxs-lookup"><span data-stu-id="d930c-138">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="d930c-139">Esempio 9: creare un contesto usando un token SAS</span><span class="sxs-lookup"><span data-stu-id="d930c-139">Example 9: Create a context by using an SAS token</span></span>
```
C:\PS>$SasToken = New-AzureStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzureStorageBlob -Container "ContosoMain"
```

<span data-ttu-id="d930c-140">Il primo comando genera un token SAS usando il cmdlet **New-AzureStorageContainerSASToken** per il contenitore denominato ContosoMain e quindi archivia tale token nella variabile $SasToken.</span><span class="sxs-lookup"><span data-stu-id="d930c-140">The first command generates an SAS token by using the **New-AzureStorageContainerSASToken** cmdlet for the container named ContosoMain, and then stores that token in the $SasToken variable.</span></span>
<span data-ttu-id="d930c-141">Il token è per le autorizzazioni di lettura, aggiunta, aggiornamento ed eliminazione.</span><span class="sxs-lookup"><span data-stu-id="d930c-141">That token is for read, add, update, and delete permissions.</span></span>
<span data-ttu-id="d930c-142">Il secondo comando crea un contesto per l'account denominato ContosoGeneral che usa il token SAS archiviato in $SasToken e quindi archivia tale contesto nella variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="d930c-142">The second command creates a context for the account named ContosoGeneral that uses the SAS token stored in $SasToken, and then stores that context in the $Context variable.</span></span>
<span data-ttu-id="d930c-143">Il comando finale elenca tutti i BLOB associati al contenitore denominato ContosoMain usando il contesto archiviato in $Context.</span><span class="sxs-lookup"><span data-stu-id="d930c-143">The final command lists all the blobs associated with the container named ContosoMain by using the context stored in $Context.</span></span>

## <span data-ttu-id="d930c-144">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d930c-144">PARAMETERS</span></span>

### <span data-ttu-id="d930c-145">-Anonimo</span><span class="sxs-lookup"><span data-stu-id="d930c-145">-Anonymous</span></span>
<span data-ttu-id="d930c-146">Indica che questo cmdlet crea un contesto di archiviazione di Azure per l'accesso anonimo.</span><span class="sxs-lookup"><span data-stu-id="d930c-146">Indicates that this cmdlet creates an Azure Storage context for anonymous logon.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AnonymousAccount, AnonymousAccountEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d930c-147">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="d930c-147">-ConnectionString</span></span>
<span data-ttu-id="d930c-148">Specifica una stringa di connessione per il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d930c-148">Specifies a connection string for the Azure Storage context.</span></span>

```yaml
Type: System.String
Parameter Sets: ConnectionString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d930c-149">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="d930c-149">-Endpoint</span></span>
<span data-ttu-id="d930c-150">Specifica l'endpoint per il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d930c-150">Specifies the endpoint for the Azure Storage context.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameAndKey, AnonymousAccount, SasToken
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d930c-151">-Ambiente</span><span class="sxs-lookup"><span data-stu-id="d930c-151">-Environment</span></span>
<span data-ttu-id="d930c-152">Specifica l'ambiente Azure.</span><span class="sxs-lookup"><span data-stu-id="d930c-152">Specifies the Azure environment.</span></span>
<span data-ttu-id="d930c-153">I valori accettabili per questo parametro sono: AzureCloud e AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="d930c-153">The acceptable values for this parameter are: AzureCloud and AzureChinaCloud.</span></span>
<span data-ttu-id="d930c-154">Per altre informazioni, digitare `Get-Help Get-AzureEnvironment` .</span><span class="sxs-lookup"><span data-stu-id="d930c-154">For more information, type `Get-Help Get-AzureEnvironment`.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameAndKeyEnvironment, AnonymousAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SasTokenWithAzureEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d930c-155">-Local</span><span class="sxs-lookup"><span data-stu-id="d930c-155">-Local</span></span>
<span data-ttu-id="d930c-156">Indica che questo cmdlet crea un contesto utilizzando l'account di archiviazione dello sviluppo locale.</span><span class="sxs-lookup"><span data-stu-id="d930c-156">Indicates that this cmdlet creates a context by using the local development storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LocalDevelopment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d930c-157">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="d930c-157">-Protocol</span></span>
<span data-ttu-id="d930c-158">Transfer Protocol (https/http).</span><span class="sxs-lookup"><span data-stu-id="d930c-158">Transfer Protocol (https/http).</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d930c-159">-SasToken</span><span class="sxs-lookup"><span data-stu-id="d930c-159">-SasToken</span></span>
<span data-ttu-id="d930c-160">Specifica un token SAS (Shared Access Signature) per il contesto.</span><span class="sxs-lookup"><span data-stu-id="d930c-160">Specifies a Shared Access Signature (SAS) token for the context.</span></span>

```yaml
Type: System.String
Parameter Sets: SasToken, SasTokenWithAzureEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d930c-161">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d930c-161">-StorageAccountKey</span></span>
<span data-ttu-id="d930c-162">Specifica una chiave dell'account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d930c-162">Specifies an Azure Storage account key.</span></span>
<span data-ttu-id="d930c-163">Questo cmdlet crea un contesto per la chiave specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="d930c-163">This cmdlet creates a context for the key that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d930c-164">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d930c-164">-StorageAccountName</span></span>
<span data-ttu-id="d930c-165">Specifica un nome dell'account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d930c-165">Specifies an Azure Storage account name.</span></span>
<span data-ttu-id="d930c-166">Questo cmdlet crea un contesto per l'account specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="d930c-166">This cmdlet creates a context for the account that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, SasTokenWithAzureEnvironment
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d930c-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d930c-167">CommonParameters</span></span>
<span data-ttu-id="d930c-168">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d930c-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d930c-169">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d930c-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d930c-170">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d930c-170">INPUTS</span></span>

### <span data-ttu-id="d930c-171">System. String</span><span class="sxs-lookup"><span data-stu-id="d930c-171">System.String</span></span>

## <span data-ttu-id="d930c-172">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d930c-172">OUTPUTS</span></span>

### <span data-ttu-id="d930c-173">Microsoft. WindowsAzure. Commands. storage. AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="d930c-173">Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext</span></span>

## <span data-ttu-id="d930c-174">Note</span><span class="sxs-lookup"><span data-stu-id="d930c-174">NOTES</span></span>

## <span data-ttu-id="d930c-175">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d930c-175">RELATED LINKS</span></span>

[<span data-ttu-id="d930c-176">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="d930c-176">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="d930c-177">New-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="d930c-177">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)


