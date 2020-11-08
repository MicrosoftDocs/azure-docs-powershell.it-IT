---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
ms.openlocfilehash: ae12bb509773f36ecfd94ad6907499f0b5feb02d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188734"
---
# <span data-ttu-id="1a238-101">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="1a238-101">New-AzStorageContext</span></span>

## <span data-ttu-id="1a238-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1a238-102">SYNOPSIS</span></span>
<span data-ttu-id="1a238-103">Crea un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="1a238-103">Creates an Azure Storage context.</span></span>

## <span data-ttu-id="1a238-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1a238-104">SYNTAX</span></span>

### <span data-ttu-id="1a238-105">OAuthAccount (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1a238-105">OAuthAccount (Default)</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="1a238-106">AccountNameAndKey</span><span class="sxs-lookup"><span data-stu-id="1a238-106">AccountNameAndKey</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="1a238-107">AccountNameAndKeyEnvironment</span><span class="sxs-lookup"><span data-stu-id="1a238-107">AccountNameAndKeyEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="1a238-108">AnonymousAccount</span><span class="sxs-lookup"><span data-stu-id="1a238-108">AnonymousAccount</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="1a238-109">AnonymousAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="1a238-109">AnonymousAccountEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="1a238-110">SasToken</span><span class="sxs-lookup"><span data-stu-id="1a238-110">SasToken</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="1a238-111">SasTokenWithAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="1a238-111">SasTokenWithAzureEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="1a238-112">OAuthAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="1a238-112">OAuthAccountEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="1a238-113">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="1a238-113">ConnectionString</span></span>
```
New-AzStorageContext -ConnectionString <String> [<CommonParameters>]
```

### <span data-ttu-id="1a238-114">LocalDevelopment</span><span class="sxs-lookup"><span data-stu-id="1a238-114">LocalDevelopment</span></span>
```
New-AzStorageContext [-Local] [<CommonParameters>]
```

## <span data-ttu-id="1a238-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a238-115">DESCRIPTION</span></span>
<span data-ttu-id="1a238-116">Il cmdlet **New-AzStorageContext** crea un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="1a238-116">The **New-AzStorageContext** cmdlet creates an Azure Storage context.</span></span>
<span data-ttu-id="1a238-117">L'autenticazione predefinita di un contesto di archiviazione è OAuth (Azure AD), se solo il nome dell'account di archiviazione di input.</span><span class="sxs-lookup"><span data-stu-id="1a238-117">The default Authentication of a Storage Context is OAuth (Azure AD), if only input Storage account name.</span></span>
<span data-ttu-id="1a238-118">Vedere i dettagli dell'autenticazione del servizio di archiviazione https://docs.microsoft.com/en-us/rest/api/storageservices/authorization-for-the-azure-storage-services .</span><span class="sxs-lookup"><span data-stu-id="1a238-118">See details of authentication of the Storage Service in https://docs.microsoft.com/en-us/rest/api/storageservices/authorization-for-the-azure-storage-services.</span></span>

## <span data-ttu-id="1a238-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1a238-119">EXAMPLES</span></span>

### <span data-ttu-id="1a238-120">Esempio 1: creare un contesto specificando un nome e una chiave dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="1a238-120">Example 1: Create a context by specifying a storage account name and key</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

<span data-ttu-id="1a238-121">Questo comando crea un contesto per l'account denominato ContosoGeneral che usa la chiave specificata.</span><span class="sxs-lookup"><span data-stu-id="1a238-121">This command creates a context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="1a238-122">Esempio 2: creare un contesto specificando una stringa di connessione</span><span class="sxs-lookup"><span data-stu-id="1a238-122">Example 2: Create a context by specifying a connection string</span></span>
```
PS C:\>New-AzStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

<span data-ttu-id="1a238-123">Questo comando crea un contesto basato sulla stringa di connessione specificata per l'account ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="1a238-123">This command creates a context based on the specified connection string for the account ContosoGeneral.</span></span>

### <span data-ttu-id="1a238-124">Esempio 3: creare un contesto per un account di archiviazione Anonimo</span><span class="sxs-lookup"><span data-stu-id="1a238-124">Example 3: Create a context for an anonymous storage account</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

<span data-ttu-id="1a238-125">Questo comando crea un contesto per l'uso anonimo per l'account denominato ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="1a238-125">This command creates a context for anonymous use for the account named ContosoGeneral.</span></span>
<span data-ttu-id="1a238-126">Il comando specifica HTTP come protocollo di connessione.</span><span class="sxs-lookup"><span data-stu-id="1a238-126">The command specifies HTTP as a connection protocol.</span></span>

### <span data-ttu-id="1a238-127">Esempio 4: creare un contesto usando l'account di archiviazione dello sviluppo locale</span><span class="sxs-lookup"><span data-stu-id="1a238-127">Example 4: Create a context by using the local development storage account</span></span>
```
PS C:\>New-AzStorageContext -Local
```

<span data-ttu-id="1a238-128">Questo comando crea un contesto usando l'account di archiviazione dello sviluppo locale.</span><span class="sxs-lookup"><span data-stu-id="1a238-128">This command creates a context by using the local development storage account.</span></span>
<span data-ttu-id="1a238-129">Il comando specifica il parametro *local* .</span><span class="sxs-lookup"><span data-stu-id="1a238-129">The command specifies the *Local* parameter.</span></span>

### <span data-ttu-id="1a238-130">Esempio 5: ottenere il contenitore per l'account di archiviazione dello sviluppatore locale</span><span class="sxs-lookup"><span data-stu-id="1a238-130">Example 5: Get the container for the local developer storage account</span></span>
```
PS C:\>New-AzStorageContext -Local | Get-AzStorageContainer
```

<span data-ttu-id="1a238-131">Questo comando crea un contesto usando l'account di archiviazione dello sviluppo locale e quindi passa il nuovo contesto al cmdlet **Get-AzStorageContainer** usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="1a238-131">This command creates a context by using the local development storage account, and then passes the new context to the **Get-AzStorageContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1a238-132">Il comando ottiene il contenitore di archiviazione di Azure per l'account di archiviazione dello sviluppatore locale.</span><span class="sxs-lookup"><span data-stu-id="1a238-132">The command gets the Azure Storage container for the local developer storage account.</span></span>

### <span data-ttu-id="1a238-133">Esempio 6: ottenere più contenitori</span><span class="sxs-lookup"><span data-stu-id="1a238-133">Example 6: Get multiple containers</span></span>
```
PS C:\>$Context01 = New-AzStorageContext -Local 
PS C:\> $Context02 = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzStorageContainer
```

<span data-ttu-id="1a238-134">Con il primo comando viene creato un contesto utilizzando l'account di archiviazione dello sviluppo locale e il contesto viene archiviato nella variabile $Context 01.</span><span class="sxs-lookup"><span data-stu-id="1a238-134">The first command creates a context by using the local development storage account, and then stores that context in the $Context01 variable.</span></span>
<span data-ttu-id="1a238-135">Il secondo comando crea un contesto per l'account denominato ContosoGeneral che usa la chiave specificata e quindi archivia tale contesto nella variabile $Context 02.</span><span class="sxs-lookup"><span data-stu-id="1a238-135">The second command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that context in the $Context02 variable.</span></span>
<span data-ttu-id="1a238-136">Il comando finale recupera i contenitori per i contesti archiviati in $Context 01 e $Context 02 usando **Get-AzStorageContainer**.</span><span class="sxs-lookup"><span data-stu-id="1a238-136">The final command gets the containers for the contexts stored in $Context01 and $Context02 by using **Get-AzStorageContainer**.</span></span>

### <span data-ttu-id="1a238-137">Esempio 7: creare un contesto con un endpoint</span><span class="sxs-lookup"><span data-stu-id="1a238-137">Example 7: Create a context with an endpoint</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

<span data-ttu-id="1a238-138">Questo comando crea un contesto di archiviazione di Azure con l'endpoint di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="1a238-138">This command creates an Azure Storage context that has the specified storage endpoint.</span></span>
<span data-ttu-id="1a238-139">Il comando crea il contesto per l'account denominato ContosoGeneral che usa la chiave specificata.</span><span class="sxs-lookup"><span data-stu-id="1a238-139">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="1a238-140">Esempio 8: creare un contesto con un ambiente specificato</span><span class="sxs-lookup"><span data-stu-id="1a238-140">Example 8: Create a context with a specified environment</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

<span data-ttu-id="1a238-141">Questo comando crea un contesto di archiviazione di Azure con l'ambiente Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="1a238-141">This command creates an Azure storage context that has the specified Azure environment.</span></span>
<span data-ttu-id="1a238-142">Il comando crea il contesto per l'account denominato ContosoGeneral che usa la chiave specificata.</span><span class="sxs-lookup"><span data-stu-id="1a238-142">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="1a238-143">Esempio 9: creare un contesto usando un token SAS</span><span class="sxs-lookup"><span data-stu-id="1a238-143">Example 9: Create a context by using an SAS token</span></span>
```
PS C:\>$SasToken = New-AzStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzStorageBlob -Container "ContosoMain"
```

<span data-ttu-id="1a238-144">Il primo comando genera un token SAS usando il cmdlet **New-AzStorageContainerSASToken** per il contenitore denominato ContosoMain e quindi archivia tale token nella variabile $SasToken.</span><span class="sxs-lookup"><span data-stu-id="1a238-144">The first command generates an SAS token by using the **New-AzStorageContainerSASToken** cmdlet for the container named ContosoMain, and then stores that token in the $SasToken variable.</span></span>
<span data-ttu-id="1a238-145">Il token è per le autorizzazioni di lettura, aggiunta, aggiornamento ed eliminazione.</span><span class="sxs-lookup"><span data-stu-id="1a238-145">That token is for read, add, update, and delete permissions.</span></span>
<span data-ttu-id="1a238-146">Il secondo comando crea un contesto per l'account denominato ContosoGeneral che usa il token SAS archiviato in $SasToken e quindi archivia tale contesto nella variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="1a238-146">The second command creates a context for the account named ContosoGeneral that uses the SAS token stored in $SasToken, and then stores that context in the $Context variable.</span></span>
<span data-ttu-id="1a238-147">Il comando finale elenca tutti i BLOB associati al contenitore denominato ContosoMain usando il contesto archiviato in $Context.</span><span class="sxs-lookup"><span data-stu-id="1a238-147">The final command lists all the blobs associated with the container named ContosoMain by using the context stored in $Context.</span></span>

### <span data-ttu-id="1a238-148">Esempio 10: creare un contesto usando l'autenticazione OAuth</span><span class="sxs-lookup"><span data-stu-id="1a238-148">Example 10: Create a context by using the OAuth Authentication</span></span>
```
PS C:\>Connect-AzAccount
PS C:\> $Context = New-AzStorageContext -StorageAccountName "myaccountname" -UseConnectedAccount
```

<span data-ttu-id="1a238-149">Questo comando crea un contesto usando l'autenticazione OAuth (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="1a238-149">This command creates a context by using the OAuth (Azure AD) Authentication.</span></span>

## <span data-ttu-id="1a238-150">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1a238-150">PARAMETERS</span></span>

### <span data-ttu-id="1a238-151">-Anonimo</span><span class="sxs-lookup"><span data-stu-id="1a238-151">-Anonymous</span></span>
<span data-ttu-id="1a238-152">Indica che questo cmdlet crea un contesto di archiviazione di Azure per l'accesso anonimo.</span><span class="sxs-lookup"><span data-stu-id="1a238-152">Indicates that this cmdlet creates an Azure Storage context for anonymous logon.</span></span>

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

### <span data-ttu-id="1a238-153">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="1a238-153">-ConnectionString</span></span>
<span data-ttu-id="1a238-154">Specifica una stringa di connessione per il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="1a238-154">Specifies a connection string for the Azure Storage context.</span></span>

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

### <span data-ttu-id="1a238-155">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="1a238-155">-Endpoint</span></span>
<span data-ttu-id="1a238-156">Specifica l'endpoint per il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="1a238-156">Specifies the endpoint for the Azure Storage context.</span></span>

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AnonymousAccount, SasToken
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a238-157">-Ambiente</span><span class="sxs-lookup"><span data-stu-id="1a238-157">-Environment</span></span>
<span data-ttu-id="1a238-158">Specifica l'ambiente Azure.</span><span class="sxs-lookup"><span data-stu-id="1a238-158">Specifies the Azure environment.</span></span>
<span data-ttu-id="1a238-159">I valori accettabili per questo parametro sono: AzureCloud e AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="1a238-159">The acceptable values for this parameter are: AzureCloud and AzureChinaCloud.</span></span>
<span data-ttu-id="1a238-160">Per altre informazioni, digitare `Get-Help Get-AzEnvironment` .</span><span class="sxs-lookup"><span data-stu-id="1a238-160">For more information, type `Get-Help Get-AzEnvironment`.</span></span>

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
Parameter Sets: SasTokenWithAzureEnvironment, OAuthAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a238-161">-Local</span><span class="sxs-lookup"><span data-stu-id="1a238-161">-Local</span></span>
<span data-ttu-id="1a238-162">Indica che questo cmdlet crea un contesto utilizzando l'account di archiviazione dello sviluppo locale.</span><span class="sxs-lookup"><span data-stu-id="1a238-162">Indicates that this cmdlet creates a context by using the local development storage account.</span></span>

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

### <span data-ttu-id="1a238-163">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="1a238-163">-Protocol</span></span>
<span data-ttu-id="1a238-164">Transfer Protocol (https/http).</span><span class="sxs-lookup"><span data-stu-id="1a238-164">Transfer Protocol (https/http).</span></span>

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, OAuthAccountEnvironment
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a238-165">-SasToken</span><span class="sxs-lookup"><span data-stu-id="1a238-165">-SasToken</span></span>
<span data-ttu-id="1a238-166">Specifica un token SAS (Shared Access Signature) per il contesto.</span><span class="sxs-lookup"><span data-stu-id="1a238-166">Specifies a Shared Access Signature (SAS) token for the context.</span></span>

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

### <span data-ttu-id="1a238-167">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="1a238-167">-StorageAccountKey</span></span>
<span data-ttu-id="1a238-168">Specifica una chiave dell'account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="1a238-168">Specifies an Azure Storage account key.</span></span>
<span data-ttu-id="1a238-169">Questo cmdlet crea un contesto per la chiave specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="1a238-169">This cmdlet creates a context for the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="1a238-170">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1a238-170">-StorageAccountName</span></span>
<span data-ttu-id="1a238-171">Specifica un nome dell'account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="1a238-171">Specifies an Azure Storage account name.</span></span>
<span data-ttu-id="1a238-172">Questo cmdlet crea un contesto per l'account specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="1a238-172">This cmdlet creates a context for the account that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, SasTokenWithAzureEnvironment, OAuthAccountEnvironment
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a238-173">-UseConnectedAccount</span><span class="sxs-lookup"><span data-stu-id="1a238-173">-UseConnectedAccount</span></span>
<span data-ttu-id="1a238-174">Indica che questo cmdlet crea un contesto di archiviazione di Azure con l'autenticazione OAuth (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="1a238-174">Indicates that this cmdlet creates an Azure Storage context with OAuth (Azure AD) Authentication.</span></span>
<span data-ttu-id="1a238-175">Il cmdlet utilizzerà l'autenticazione OAuth per impostazione predefinita, quando non viene specificata un'altra autenticazione.</span><span class="sxs-lookup"><span data-stu-id="1a238-175">The cmdlet will use OAuth Authentication by default, when other authentication not specified.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OAuthAccount, OAuthAccountEnvironment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a238-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a238-176">CommonParameters</span></span>
<span data-ttu-id="1a238-177">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a238-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a238-178">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a238-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a238-179">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1a238-179">INPUTS</span></span>

### <span data-ttu-id="1a238-180">System. String</span><span class="sxs-lookup"><span data-stu-id="1a238-180">System.String</span></span>

## <span data-ttu-id="1a238-181">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1a238-181">OUTPUTS</span></span>

### <span data-ttu-id="1a238-182">Microsoft. WindowsAzure. Commands. storage. AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="1a238-182">Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext</span></span>

## <span data-ttu-id="1a238-183">Note</span><span class="sxs-lookup"><span data-stu-id="1a238-183">NOTES</span></span>

## <span data-ttu-id="1a238-184">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1a238-184">RELATED LINKS</span></span>

[<span data-ttu-id="1a238-185">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="1a238-185">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="1a238-186">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="1a238-186">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)


