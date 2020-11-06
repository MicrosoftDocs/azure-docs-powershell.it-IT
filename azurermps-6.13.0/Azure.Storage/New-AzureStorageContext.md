---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContext.md
ms.openlocfilehash: 9de6b2b52205bdf80de9c57e3e338f4b7216c5ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517784"
---
# <span data-ttu-id="7c1e6-101">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="7c1e6-101">New-AzureStorageContext</span></span>

## <span data-ttu-id="7c1e6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7c1e6-102">SYNOPSIS</span></span>
<span data-ttu-id="7c1e6-103">Crea un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="7c1e6-103">Creates an Azure Storage context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c1e6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7c1e6-104">SYNTAX</span></span>

### <span data-ttu-id="7c1e6-105">OAuthAccount (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7c1e6-105">OAuthAccount (Default)</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="7c1e6-106">AccountNameAndKey</span><span class="sxs-lookup"><span data-stu-id="7c1e6-106">AccountNameAndKey</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="7c1e6-107">AccountNameAndKeyEnvironment</span><span class="sxs-lookup"><span data-stu-id="7c1e6-107">AccountNameAndKeyEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="7c1e6-108">AnonymousAccount</span><span class="sxs-lookup"><span data-stu-id="7c1e6-108">AnonymousAccount</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="7c1e6-109">AnonymousAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="7c1e6-109">AnonymousAccountEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="7c1e6-110">SasToken</span><span class="sxs-lookup"><span data-stu-id="7c1e6-110">SasToken</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="7c1e6-111">SasTokenWithAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="7c1e6-111">SasTokenWithAzureEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="7c1e6-112">OAuthAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="7c1e6-112">OAuthAccountEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="7c1e6-113">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="7c1e6-113">ConnectionString</span></span>
```
New-AzureStorageContext -ConnectionString <String> [<CommonParameters>]
```

### <span data-ttu-id="7c1e6-114">LocalDevelopment</span><span class="sxs-lookup"><span data-stu-id="7c1e6-114">LocalDevelopment</span></span>
```
New-AzureStorageContext [-Local] [<CommonParameters>]
```

## <span data-ttu-id="7c1e6-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7c1e6-115">DESCRIPTION</span></span>
<span data-ttu-id="7c1e6-116">Il cmdlet **New-AzureStorageContext** crea un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="7c1e6-116">The **New-AzureStorageContext** cmdlet creates an Azure Storage context.</span></span>

## <span data-ttu-id="7c1e6-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7c1e6-117">EXAMPLES</span></span>

### <span data-ttu-id="7c1e6-118">Esempio 1: creare un contesto specificando un nome e una chiave dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="7c1e6-118">Example 1: Create a context by specifying a storage account name and key</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

<span data-ttu-id="7c1e6-119">Questo comando crea un contesto per l'account denominato ContosoGeneral che usa la chiave specificata.</span><span class="sxs-lookup"><span data-stu-id="7c1e6-119">This command creates a context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="7c1e6-120">Esempio 2: creare un contesto specificando una stringa di connessione</span><span class="sxs-lookup"><span data-stu-id="7c1e6-120">Example 2: Create a context by specifying a connection string</span></span>
```
C:\PS>New-AzureStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

<span data-ttu-id="7c1e6-121">Questo comando crea un contesto basato sulla stringa di connessione specificata per l'account ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="7c1e6-121">This command creates a context based on the specified connection string for the account ContosoGeneral.</span></span>

### <span data-ttu-id="7c1e6-122">Esempio 3: creare un contesto per un account di archiviazione Anonimo</span><span class="sxs-lookup"><span data-stu-id="7c1e6-122">Example 3: Create a context for an anonymous storage account</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

<span data-ttu-id="7c1e6-123">Questo comando crea un contesto per l'uso anonimo per l'account denominato ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="7c1e6-123">This command creates a context for anonymous use for the account named ContosoGeneral.</span></span>
<span data-ttu-id="7c1e6-124">Il comando specifica HTTP come protocollo di connessione.</span><span class="sxs-lookup"><span data-stu-id="7c1e6-124">The command specifies HTTP as a connection protocol.</span></span>

### <span data-ttu-id="7c1e6-125">Esempio 4: creare un contesto usando l'account di archiviazione dello sviluppo locale</span><span class="sxs-lookup"><span data-stu-id="7c1e6-125">Example 4: Create a context by using the local development storage account</span></span>
```
C:\PS>New-AzureStorageContext -Local
```

<span data-ttu-id="7c1e6-126">Questo comando crea un contesto usando l'account di archiviazione dello sviluppo locale.</span><span class="sxs-lookup"><span data-stu-id="7c1e6-126">This command creates a context by using the local development storage account.</span></span>
<span data-ttu-id="7c1e6-127">Il comando specifica il parametro *local* .</span><span class="sxs-lookup"><span data-stu-id="7c1e6-127">The command specifies the *Local* parameter.</span></span>

### <span data-ttu-id="7c1e6-128">Esempio 5: ottenere il contenitore per l'account di archiviazione dello sviluppatore locale</span><span class="sxs-lookup"><span data-stu-id="7c1e6-128">Example 5: Get the container for the local developer storage account</span></span>
```
C:\PS>New-AzureStorageContext -Local | Get-AzureStorageContainer
```

<span data-ttu-id="7c1e6-129">Questo comando crea un contesto usando l'account di archiviazione dello sviluppo locale e quindi passa il nuovo contesto al cmdlet **Get-AzureStorageContainer** usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="7c1e6-129">This command creates a context by using the local development storage account, and then passes the new context to the **Get-AzureStorageContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7c1e6-130">Il comando ottiene il contenitore di archiviazione di Azure per l'account di archiviazione dello sviluppatore locale.</span><span class="sxs-lookup"><span data-stu-id="7c1e6-130">The command gets the Azure Storage container for the local developer storage account.</span></span>

### <span data-ttu-id="7c1e6-131">Esempio 6: ottenere più contenitori</span><span class="sxs-lookup"><span data-stu-id="7c1e6-131">Example 6: Get multiple containers</span></span>
```
C:\PS>$Context01 = New-AzureStorageContext -Local 
PS C:\> $Context02 = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzureStorageContainer
```

<span data-ttu-id="7c1e6-132">Con il primo comando viene creato un contesto utilizzando l'account di archiviazione dello sviluppo locale e il contesto viene archiviato nella variabile $Context 01.</span><span class="sxs-lookup"><span data-stu-id="7c1e6-132">The first command creates a context by using the local development storage account, and then stores that context in the $Context01 variable.</span></span>
<span data-ttu-id="7c1e6-133">Il secondo comando crea un contesto per l'account denominato ContosoGeneral che usa la chiave specificata e quindi archivia tale contesto nella variabile $Context 02.</span><span class="sxs-lookup"><span data-stu-id="7c1e6-133">The second command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that context in the $Context02 variable.</span></span>
<span data-ttu-id="7c1e6-134">Il comando finale recupera i contenitori per i contesti archiviati in $Context 01 e $Context 02 usando **Get-AzureStorageContainer**.</span><span class="sxs-lookup"><span data-stu-id="7c1e6-134">The final command gets the containers for the contexts stored in $Context01 and $Context02 by using **Get-AzureStorageContainer**.</span></span>

### <span data-ttu-id="7c1e6-135">Esempio 7: creare un contesto con un endpoint</span><span class="sxs-lookup"><span data-stu-id="7c1e6-135">Example 7: Create a context with an endpoint</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

<span data-ttu-id="7c1e6-136">Questo comando crea un contesto di archiviazione di Azure con l'endpoint di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="7c1e6-136">This command creates an Azure Storage context that has the specified storage endpoint.</span></span>
<span data-ttu-id="7c1e6-137">Il comando crea il contesto per l'account denominato ContosoGeneral che usa la chiave specificata.</span><span class="sxs-lookup"><span data-stu-id="7c1e6-137">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="7c1e6-138">Esempio 8: creare un contesto con un ambiente specificato</span><span class="sxs-lookup"><span data-stu-id="7c1e6-138">Example 8: Create a context with a specified environment</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

<span data-ttu-id="7c1e6-139">Questo comando crea un contesto di archiviazione di Azure con l'ambiente Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="7c1e6-139">This command creates an Azure storage context that has the specified Azure environment.</span></span>
<span data-ttu-id="7c1e6-140">Il comando crea il contesto per l'account denominato ContosoGeneral che usa la chiave specificata.</span><span class="sxs-lookup"><span data-stu-id="7c1e6-140">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="7c1e6-141">Esempio 9: creare un contesto usando un token SAS</span><span class="sxs-lookup"><span data-stu-id="7c1e6-141">Example 9: Create a context by using an SAS token</span></span>
```
C:\PS>$SasToken = New-AzureStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzureStorageBlob -Container "ContosoMain"
```

<span data-ttu-id="7c1e6-142">Il primo comando genera un token SAS usando il cmdlet **New-AzureStorageContainerSASToken** per il contenitore denominato ContosoMain e quindi archivia tale token nella variabile $SasToken.</span><span class="sxs-lookup"><span data-stu-id="7c1e6-142">The first command generates an SAS token by using the **New-AzureStorageContainerSASToken** cmdlet for the container named ContosoMain, and then stores that token in the $SasToken variable.</span></span>
<span data-ttu-id="7c1e6-143">Il token è per le autorizzazioni di lettura, aggiunta, aggiornamento ed eliminazione.</span><span class="sxs-lookup"><span data-stu-id="7c1e6-143">That token is for read, add, update, and delete permissions.</span></span>
<span data-ttu-id="7c1e6-144">Il secondo comando crea un contesto per l'account denominato ContosoGeneral che usa il token SAS archiviato in $SasToken e quindi archivia tale contesto nella variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="7c1e6-144">The second command creates a context for the account named ContosoGeneral that uses the SAS token stored in $SasToken, and then stores that context in the $Context variable.</span></span>
<span data-ttu-id="7c1e6-145">Il comando finale elenca tutti i BLOB associati al contenitore denominato ContosoMain usando il contesto archiviato in $Context.</span><span class="sxs-lookup"><span data-stu-id="7c1e6-145">The final command lists all the blobs associated with the container named ContosoMain by using the context stored in $Context.</span></span>

### <span data-ttu-id="7c1e6-146">Esempio 10: creare un contesto usando l'autenticazione OAuth</span><span class="sxs-lookup"><span data-stu-id="7c1e6-146">Example 10: Create a context by using the OAuth Authentication</span></span>
```
C:\PS>Connect-AzureRmAccount
C:\PS> $Context = New-AzureStorageContext -StorageAccountName "myaccountname" -UseConnectedAccount
```

<span data-ttu-id="7c1e6-147">Questo comando crea un contesto usando l'autenticazione OAuth.</span><span class="sxs-lookup"><span data-stu-id="7c1e6-147">This command creates a context by using the OAuth Authentication.</span></span>

## <span data-ttu-id="7c1e6-148">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7c1e6-148">PARAMETERS</span></span>

### <span data-ttu-id="7c1e6-149">-Anonimo</span><span class="sxs-lookup"><span data-stu-id="7c1e6-149">-Anonymous</span></span>
<span data-ttu-id="7c1e6-150">Indica che questo cmdlet crea un contesto di archiviazione di Azure per l'accesso anonimo.</span><span class="sxs-lookup"><span data-stu-id="7c1e6-150">Indicates that this cmdlet creates an Azure Storage context for anonymous logon.</span></span>

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

### <span data-ttu-id="7c1e6-151">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="7c1e6-151">-ConnectionString</span></span>
<span data-ttu-id="7c1e6-152">Specifica una stringa di connessione per il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="7c1e6-152">Specifies a connection string for the Azure Storage context.</span></span>

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

### <span data-ttu-id="7c1e6-153">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="7c1e6-153">-Endpoint</span></span>
<span data-ttu-id="7c1e6-154">Specifica l'endpoint per il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="7c1e6-154">Specifies the endpoint for the Azure Storage context.</span></span>

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

### <span data-ttu-id="7c1e6-155">-Ambiente</span><span class="sxs-lookup"><span data-stu-id="7c1e6-155">-Environment</span></span>
<span data-ttu-id="7c1e6-156">Specifica l'ambiente Azure.</span><span class="sxs-lookup"><span data-stu-id="7c1e6-156">Specifies the Azure environment.</span></span>
<span data-ttu-id="7c1e6-157">I valori accettabili per questo parametro sono: AzureCloud e AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="7c1e6-157">The acceptable values for this parameter are: AzureCloud and AzureChinaCloud.</span></span>
<span data-ttu-id="7c1e6-158">Per altre informazioni, digitare `Get-Help Get-AzureEnvironment` .</span><span class="sxs-lookup"><span data-stu-id="7c1e6-158">For more information, type `Get-Help Get-AzureEnvironment`.</span></span>

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

### <span data-ttu-id="7c1e6-159">-Local</span><span class="sxs-lookup"><span data-stu-id="7c1e6-159">-Local</span></span>
<span data-ttu-id="7c1e6-160">Indica che questo cmdlet crea un contesto utilizzando l'account di archiviazione dello sviluppo locale.</span><span class="sxs-lookup"><span data-stu-id="7c1e6-160">Indicates that this cmdlet creates a context by using the local development storage account.</span></span>

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

### <span data-ttu-id="7c1e6-161">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="7c1e6-161">-Protocol</span></span>
<span data-ttu-id="7c1e6-162">Transfer Protocol (https/http).</span><span class="sxs-lookup"><span data-stu-id="7c1e6-162">Transfer Protocol (https/http).</span></span>

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

### <span data-ttu-id="7c1e6-163">-SasToken</span><span class="sxs-lookup"><span data-stu-id="7c1e6-163">-SasToken</span></span>
<span data-ttu-id="7c1e6-164">Specifica un token SAS (Shared Access Signature) per il contesto.</span><span class="sxs-lookup"><span data-stu-id="7c1e6-164">Specifies a Shared Access Signature (SAS) token for the context.</span></span>

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

### <span data-ttu-id="7c1e6-165">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="7c1e6-165">-StorageAccountKey</span></span>
<span data-ttu-id="7c1e6-166">Specifica una chiave dell'account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="7c1e6-166">Specifies an Azure Storage account key.</span></span>
<span data-ttu-id="7c1e6-167">Questo cmdlet crea un contesto per la chiave specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="7c1e6-167">This cmdlet creates a context for the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="7c1e6-168">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7c1e6-168">-StorageAccountName</span></span>
<span data-ttu-id="7c1e6-169">Specifica un nome dell'account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="7c1e6-169">Specifies an Azure Storage account name.</span></span>
<span data-ttu-id="7c1e6-170">Questo cmdlet crea un contesto per l'account specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="7c1e6-170">This cmdlet creates a context for the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="7c1e6-171">-UseConnectedAccount</span><span class="sxs-lookup"><span data-stu-id="7c1e6-171">-UseConnectedAccount</span></span>
<span data-ttu-id="7c1e6-172">Indica che questo cmdlet crea un contesto di archiviazione di Azure con l'autenticazione OAuth.</span><span class="sxs-lookup"><span data-stu-id="7c1e6-172">Indicates that this cmdlet creates an Azure Storage context with OAuth Authentication.</span></span>
<span data-ttu-id="7c1e6-173">Il cmdlet utilizzerà l'autenticazione OAuth per impostazione predefinita, quando gli altri anthentication non sono specificati.</span><span class="sxs-lookup"><span data-stu-id="7c1e6-173">The cmdlet will use OAuth Authentication by default, when other anthentication not specified.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: OAuthAccount, OAuthAccountEnvironment
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c1e6-174">-UseConnectedAccount</span><span class="sxs-lookup"><span data-stu-id="7c1e6-174">-UseConnectedAccount</span></span>
<span data-ttu-id="7c1e6-175">Indica che questo cmdlet crea un contesto di archiviazione di Azure con l'autenticazione OAuth.</span><span class="sxs-lookup"><span data-stu-id="7c1e6-175">Indicates that this cmdlet creates an Azure Storage context with OAuth Authentication.</span></span>
<span data-ttu-id="7c1e6-176">Il cmdlet utilizzerà l'autenticazione OAuth per impostazione predefinita, quando gli altri anthentication non sono specificati.</span><span class="sxs-lookup"><span data-stu-id="7c1e6-176">The cmdlet will use OAuth Authentication by default, when other anthentication not specified.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: OAuthAccount, OAuthAccountEnvironment
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c1e6-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c1e6-177">CommonParameters</span></span>
<span data-ttu-id="7c1e6-178">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c1e6-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c1e6-179">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c1e6-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c1e6-180">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7c1e6-180">INPUTS</span></span>

### <span data-ttu-id="7c1e6-181">System. String</span><span class="sxs-lookup"><span data-stu-id="7c1e6-181">System.String</span></span>

## <span data-ttu-id="7c1e6-182">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7c1e6-182">OUTPUTS</span></span>

### <span data-ttu-id="7c1e6-183">Microsoft. WindowsAzure. Commands. storage. AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="7c1e6-183">Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext</span></span>

## <span data-ttu-id="7c1e6-184">Note</span><span class="sxs-lookup"><span data-stu-id="7c1e6-184">NOTES</span></span>

## <span data-ttu-id="7c1e6-185">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7c1e6-185">RELATED LINKS</span></span>

[<span data-ttu-id="7c1e6-186">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="7c1e6-186">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="7c1e6-187">New-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="7c1e6-187">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)


