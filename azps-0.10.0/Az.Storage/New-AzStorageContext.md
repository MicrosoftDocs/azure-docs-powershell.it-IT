---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageContext.md
ms.openlocfilehash: ae22e6923a03864b9371ccdf5379ef9b6bf5189d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862162"
---
# <span data-ttu-id="e5d60-101">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="e5d60-101">New-AzStorageContext</span></span>

## <span data-ttu-id="e5d60-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e5d60-102">SYNOPSIS</span></span>
<span data-ttu-id="e5d60-103">Crea un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e5d60-103">Creates an Azure Storage context.</span></span>

## <span data-ttu-id="e5d60-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e5d60-104">SYNTAX</span></span>

### <span data-ttu-id="e5d60-105">AccountNameAndKey (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e5d60-105">AccountNameAndKey (Default)</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="e5d60-106">AccountNameAndKeyEnvironment</span><span class="sxs-lookup"><span data-stu-id="e5d60-106">AccountNameAndKeyEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="e5d60-107">AnonymousAccount</span><span class="sxs-lookup"><span data-stu-id="e5d60-107">AnonymousAccount</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="e5d60-108">AnonymousAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="e5d60-108">AnonymousAccountEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="e5d60-109">SasToken</span><span class="sxs-lookup"><span data-stu-id="e5d60-109">SasToken</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="e5d60-110">SasTokenWithAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="e5d60-110">SasTokenWithAzureEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="e5d60-111">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="e5d60-111">ConnectionString</span></span>
```
New-AzStorageContext -ConnectionString <String> [<CommonParameters>]
```

### <span data-ttu-id="e5d60-112">LocalDevelopment</span><span class="sxs-lookup"><span data-stu-id="e5d60-112">LocalDevelopment</span></span>
```
New-AzStorageContext [-Local] [<CommonParameters>]
```

## <span data-ttu-id="e5d60-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e5d60-113">DESCRIPTION</span></span>
<span data-ttu-id="e5d60-114">Il cmdlet **New-AzStorageContext** crea un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e5d60-114">The **New-AzStorageContext** cmdlet creates an Azure Storage context.</span></span>

## <span data-ttu-id="e5d60-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e5d60-115">EXAMPLES</span></span>

### <span data-ttu-id="e5d60-116">Esempio 1: creare un contesto specificando un nome e una chiave dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="e5d60-116">Example 1: Create a context by specifying a storage account name and key</span></span>
```
C:\PS>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

<span data-ttu-id="e5d60-117">Questo comando crea un contesto per l'account denominato ContosoGeneral che usa la chiave specificata.</span><span class="sxs-lookup"><span data-stu-id="e5d60-117">This command creates a context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="e5d60-118">Esempio 2: creare un contesto specificando una stringa di connessione</span><span class="sxs-lookup"><span data-stu-id="e5d60-118">Example 2: Create a context by specifying a connection string</span></span>
```
C:\PS>New-AzStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

<span data-ttu-id="e5d60-119">Questo comando crea un contesto basato sulla stringa di connessione specificata per l'account ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="e5d60-119">This command creates a context based on the specified connection string for the account ContosoGeneral.</span></span>

### <span data-ttu-id="e5d60-120">Esempio 3: creare un contesto per un account di archiviazione Anonimo</span><span class="sxs-lookup"><span data-stu-id="e5d60-120">Example 3: Create a context for an anonymous storage account</span></span>
```
C:\PS>New-AzStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

<span data-ttu-id="e5d60-121">Questo comando crea un contesto per l'uso anonimo per l'account denominato ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="e5d60-121">This command creates a context for anonymous use for the account named ContosoGeneral.</span></span>
<span data-ttu-id="e5d60-122">Il comando specifica HTTP come protocollo di connessione.</span><span class="sxs-lookup"><span data-stu-id="e5d60-122">The command specifies HTTP as a connection protocol.</span></span>

### <span data-ttu-id="e5d60-123">Esempio 4: creare un contesto usando l'account di archiviazione dello sviluppo locale</span><span class="sxs-lookup"><span data-stu-id="e5d60-123">Example 4: Create a context by using the local development storage account</span></span>
```
C:\PS>New-AzStorageContext -Local
```

<span data-ttu-id="e5d60-124">Questo comando crea un contesto usando l'account di archiviazione dello sviluppo locale.</span><span class="sxs-lookup"><span data-stu-id="e5d60-124">This command creates a context by using the local development storage account.</span></span>
<span data-ttu-id="e5d60-125">Il comando specifica il parametro *local* .</span><span class="sxs-lookup"><span data-stu-id="e5d60-125">The command specifies the *Local* parameter.</span></span>

### <span data-ttu-id="e5d60-126">Esempio 5: ottenere il contenitore per l'account di archiviazione dello sviluppatore locale</span><span class="sxs-lookup"><span data-stu-id="e5d60-126">Example 5: Get the container for the local developer storage account</span></span>
```
C:\PS>New-AzStorageContext -Local | Get-AzStorageContainer
```

<span data-ttu-id="e5d60-127">Questo comando crea un contesto usando l'account di archiviazione dello sviluppo locale e quindi passa il nuovo contesto al cmdlet **Get-AzStorageContainer** usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="e5d60-127">This command creates a context by using the local development storage account, and then passes the new context to the **Get-AzStorageContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e5d60-128">Il comando ottiene il contenitore di archiviazione di Azure per l'account di archiviazione dello sviluppatore locale.</span><span class="sxs-lookup"><span data-stu-id="e5d60-128">The command gets the Azure Storage container for the local developer storage account.</span></span>

### <span data-ttu-id="e5d60-129">Esempio 6: ottenere più contenitori</span><span class="sxs-lookup"><span data-stu-id="e5d60-129">Example 6: Get multiple containers</span></span>
```
C:\PS>$Context01 = New-AzStorageContext -Local 
PS C:\> $Context02 = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzStorageContainer
```

<span data-ttu-id="e5d60-130">Con il primo comando viene creato un contesto utilizzando l'account di archiviazione dello sviluppo locale e il contesto viene archiviato nella variabile $Context 01.</span><span class="sxs-lookup"><span data-stu-id="e5d60-130">The first command creates a context by using the local development storage account, and then stores that context in the $Context01 variable.</span></span>
<span data-ttu-id="e5d60-131">Il secondo comando crea un contesto per l'account denominato ContosoGeneral che usa la chiave specificata e quindi archivia tale contesto nella variabile $Context 02.</span><span class="sxs-lookup"><span data-stu-id="e5d60-131">The second command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that context in the $Context02 variable.</span></span>
<span data-ttu-id="e5d60-132">Il comando finale recupera i contenitori per i contesti archiviati in $Context 01 e $Context 02 usando **Get-AzStorageContainer**.</span><span class="sxs-lookup"><span data-stu-id="e5d60-132">The final command gets the containers for the contexts stored in $Context01 and $Context02 by using **Get-AzStorageContainer**.</span></span>

### <span data-ttu-id="e5d60-133">Esempio 7: creare un contesto con un endpoint</span><span class="sxs-lookup"><span data-stu-id="e5d60-133">Example 7: Create a context with an endpoint</span></span>
```
C:\PS>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

<span data-ttu-id="e5d60-134">Questo comando crea un contesto di archiviazione di Azure con l'endpoint di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="e5d60-134">This command creates an Azure Storage context that has the specified storage endpoint.</span></span>
<span data-ttu-id="e5d60-135">Il comando crea il contesto per l'account denominato ContosoGeneral che usa la chiave specificata.</span><span class="sxs-lookup"><span data-stu-id="e5d60-135">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="e5d60-136">Esempio 8: creare un contesto con un ambiente specificato</span><span class="sxs-lookup"><span data-stu-id="e5d60-136">Example 8: Create a context with a specified environment</span></span>
```
C:\PS>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

<span data-ttu-id="e5d60-137">Questo comando crea un contesto di archiviazione di Azure con l'ambiente Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="e5d60-137">This command creates an Azure storage context that has the specified Azure environment.</span></span>
<span data-ttu-id="e5d60-138">Il comando crea il contesto per l'account denominato ContosoGeneral che usa la chiave specificata.</span><span class="sxs-lookup"><span data-stu-id="e5d60-138">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="e5d60-139">Esempio 9: creare un contesto usando un token SAS</span><span class="sxs-lookup"><span data-stu-id="e5d60-139">Example 9: Create a context by using an SAS token</span></span>
```
C:\PS>$SasToken = New-AzStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzStorageBlob -Container "ContosoMain"
```

<span data-ttu-id="e5d60-140">Il primo comando genera un token SAS usando il cmdlet **New-AzStorageContainerSASToken** per il contenitore denominato ContosoMain e quindi archivia tale token nella variabile $SasToken.</span><span class="sxs-lookup"><span data-stu-id="e5d60-140">The first command generates an SAS token by using the **New-AzStorageContainerSASToken** cmdlet for the container named ContosoMain, and then stores that token in the $SasToken variable.</span></span>
<span data-ttu-id="e5d60-141">Il token è per le autorizzazioni di lettura, aggiunta, aggiornamento ed eliminazione.</span><span class="sxs-lookup"><span data-stu-id="e5d60-141">That token is for read, add, update, and delete permissions.</span></span>
<span data-ttu-id="e5d60-142">Il secondo comando crea un contesto per l'account denominato ContosoGeneral che usa il token SAS archiviato in $SasToken e quindi archivia tale contesto nella variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="e5d60-142">The second command creates a context for the account named ContosoGeneral that uses the SAS token stored in $SasToken, and then stores that context in the $Context variable.</span></span>
<span data-ttu-id="e5d60-143">Il comando finale elenca tutti i BLOB associati al contenitore denominato ContosoMain usando il contesto archiviato in $Context.</span><span class="sxs-lookup"><span data-stu-id="e5d60-143">The final command lists all the blobs associated with the container named ContosoMain by using the context stored in $Context.</span></span>

## <span data-ttu-id="e5d60-144">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e5d60-144">PARAMETERS</span></span>

### <span data-ttu-id="e5d60-145">-Anonimo</span><span class="sxs-lookup"><span data-stu-id="e5d60-145">-Anonymous</span></span>
<span data-ttu-id="e5d60-146">Indica che questo cmdlet crea un contesto di archiviazione di Azure per l'accesso anonimo.</span><span class="sxs-lookup"><span data-stu-id="e5d60-146">Indicates that this cmdlet creates an Azure Storage context for anonymous logon.</span></span>

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

### <span data-ttu-id="e5d60-147">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="e5d60-147">-ConnectionString</span></span>
<span data-ttu-id="e5d60-148">Specifica una stringa di connessione per il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e5d60-148">Specifies a connection string for the Azure Storage context.</span></span>

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

### <span data-ttu-id="e5d60-149">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="e5d60-149">-Endpoint</span></span>
<span data-ttu-id="e5d60-150">Specifica l'endpoint per il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e5d60-150">Specifies the endpoint for the Azure Storage context.</span></span>

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

### <span data-ttu-id="e5d60-151">-Ambiente</span><span class="sxs-lookup"><span data-stu-id="e5d60-151">-Environment</span></span>
<span data-ttu-id="e5d60-152">Specifica l'ambiente Azure.</span><span class="sxs-lookup"><span data-stu-id="e5d60-152">Specifies the Azure environment.</span></span>
<span data-ttu-id="e5d60-153">I valori accettabili per questo parametro sono: AzureCloud e AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="e5d60-153">The acceptable values for this parameter are: AzureCloud and AzureChinaCloud.</span></span>
<span data-ttu-id="e5d60-154">Per altre informazioni, digitare `Get-Help Get-AzureEnvironment` .</span><span class="sxs-lookup"><span data-stu-id="e5d60-154">For more information, type `Get-Help Get-AzureEnvironment`.</span></span>

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

### <span data-ttu-id="e5d60-155">-Local</span><span class="sxs-lookup"><span data-stu-id="e5d60-155">-Local</span></span>
<span data-ttu-id="e5d60-156">Indica che questo cmdlet crea un contesto utilizzando l'account di archiviazione dello sviluppo locale.</span><span class="sxs-lookup"><span data-stu-id="e5d60-156">Indicates that this cmdlet creates a context by using the local development storage account.</span></span>

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

### <span data-ttu-id="e5d60-157">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="e5d60-157">-Protocol</span></span>
<span data-ttu-id="e5d60-158">Transfer Protocol (https/http).</span><span class="sxs-lookup"><span data-stu-id="e5d60-158">Transfer Protocol (https/http).</span></span>

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

### <span data-ttu-id="e5d60-159">-SasToken</span><span class="sxs-lookup"><span data-stu-id="e5d60-159">-SasToken</span></span>
<span data-ttu-id="e5d60-160">Specifica un token SAS (Shared Access Signature) per il contesto.</span><span class="sxs-lookup"><span data-stu-id="e5d60-160">Specifies a Shared Access Signature (SAS) token for the context.</span></span>

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

### <span data-ttu-id="e5d60-161">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="e5d60-161">-StorageAccountKey</span></span>
<span data-ttu-id="e5d60-162">Specifica una chiave dell'account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e5d60-162">Specifies an Azure Storage account key.</span></span>
<span data-ttu-id="e5d60-163">Questo cmdlet crea un contesto per la chiave specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="e5d60-163">This cmdlet creates a context for the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="e5d60-164">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e5d60-164">-StorageAccountName</span></span>
<span data-ttu-id="e5d60-165">Specifica un nome dell'account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e5d60-165">Specifies an Azure Storage account name.</span></span>
<span data-ttu-id="e5d60-166">Questo cmdlet crea un contesto per l'account specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="e5d60-166">This cmdlet creates a context for the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="e5d60-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5d60-167">CommonParameters</span></span>
<span data-ttu-id="e5d60-168">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5d60-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5d60-169">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5d60-169">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5d60-170">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e5d60-170">INPUTS</span></span>

### <span data-ttu-id="e5d60-171">System. String</span><span class="sxs-lookup"><span data-stu-id="e5d60-171">System.String</span></span>

## <span data-ttu-id="e5d60-172">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e5d60-172">OUTPUTS</span></span>

### <span data-ttu-id="e5d60-173">Microsoft. WindowsAzure. Commands. storage. AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="e5d60-173">Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext</span></span>

## <span data-ttu-id="e5d60-174">Note</span><span class="sxs-lookup"><span data-stu-id="e5d60-174">NOTES</span></span>

## <span data-ttu-id="e5d60-175">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e5d60-175">RELATED LINKS</span></span>

[<span data-ttu-id="e5d60-176">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="e5d60-176">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="e5d60-177">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="e5d60-177">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)


