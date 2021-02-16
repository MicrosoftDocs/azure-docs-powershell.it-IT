---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: BB6AF5A9-49BD-4A76-9F3F-44B62D2AB842
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/new-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 4f7a391228529cdb28951b6b3f3f792e8d0de395
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204394"
---
# <span data-ttu-id="4da1a-101">New-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="4da1a-101">New-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="4da1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4da1a-102">SYNOPSIS</span></span>
<span data-ttu-id="4da1a-103">Crea una nuova credenziali del catalogo di Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="4da1a-103">Creates a new Azure Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="4da1a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4da1a-104">SYNTAX</span></span>

### <span data-ttu-id="4da1a-105">CreateByHostNameAndPort (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4da1a-105">CreateByHostNameAndPort (Default)</span></span>
```
New-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4da1a-106">CreateByFullURI</span><span class="sxs-lookup"><span data-stu-id="4da1a-106">CreateByFullURI</span></span>
```
New-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-DatabaseHost] <String> [-Port] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4da1a-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4da1a-107">DESCRIPTION</span></span>
<span data-ttu-id="4da1a-108">Il cmdlet New-AzDataLakeAnalyticsCatalogCredential crea una nuova credenziali da usare in un catalogo di Azure Data Lake Analytics per la connessione a origini dati esterne.</span><span class="sxs-lookup"><span data-stu-id="4da1a-108">The New-AzDataLakeAnalyticsCatalogCredential cmdlet creates a new credential to use in an Azure Data Lake Analytics catalog for connecting to external data sources.</span></span>

## <span data-ttu-id="4da1a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4da1a-109">EXAMPLES</span></span>

### <span data-ttu-id="4da1a-110">Esempio 1: Creare le credenziali per un catalogo specificando host e porta</span><span class="sxs-lookup"><span data-stu-id="4da1a-110">Example 1: Create a credential for a catalog specifying host and port</span></span>
```
PS C:\> New-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -DatabaseHost "example.contoso.com" -Port 8080
```

<span data-ttu-id="4da1a-111">Questo comando crea le credenziali specificate per l'account, il database, l'host e la porta specificati usando il protocollo https.</span><span class="sxs-lookup"><span data-stu-id="4da1a-111">This command creates the specified credential for the specified account, database, host and port using https protocol.</span></span>

### <span data-ttu-id="4da1a-112">Esempio 2: Creare le credenziali per un catalogo che specifica l'URI completo</span><span class="sxs-lookup"><span data-stu-id="4da1a-112">Example 2: Create a credential for a catalog specifying full URI</span></span>
```
PS C:\> New-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -Uri "http://httpExample.contoso.com:8080"
```

<span data-ttu-id="4da1a-113">Questo comando crea le credenziali specificate per l'URI dell'account, del database e dell'origine dati esterna specificati.</span><span class="sxs-lookup"><span data-stu-id="4da1a-113">This command creates the specified credential for the specified account, database and external data source URI.</span></span>

## <span data-ttu-id="4da1a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4da1a-114">PARAMETERS</span></span>

### <span data-ttu-id="4da1a-115">-Account</span><span class="sxs-lookup"><span data-stu-id="4da1a-115">-Account</span></span>
<span data-ttu-id="4da1a-116">Specifica il nome dell'account Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="4da1a-116">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4da1a-117">-Credential</span><span class="sxs-lookup"><span data-stu-id="4da1a-117">-Credential</span></span>
<span data-ttu-id="4da1a-118">Specifica il nome utente e la password corrispondente delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="4da1a-118">Specifies the user name and corresponding password of the credential.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4da1a-119">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="4da1a-119">-CredentialName</span></span>
<span data-ttu-id="4da1a-120">Specifica il nome e la password delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="4da1a-120">Specifies the name and password of the credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4da1a-121">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="4da1a-121">-DatabaseHost</span></span>
<span data-ttu-id="4da1a-122">Specifica il nome host dell'origine dati esterna a cui le credenziali possono connettersi nel formato mydatabase.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="4da1a-122">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByFullURI
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4da1a-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4da1a-123">-DatabaseName</span></span>
<span data-ttu-id="4da1a-124">Specifica il nome del database nell'account Data Lake Analytics in cui verranno archiviate le credenziali.</span><span class="sxs-lookup"><span data-stu-id="4da1a-124">Specifies the name of the database in the Data Lake Analytics account that the credential will be stored in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4da1a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4da1a-125">-DefaultProfile</span></span>
<span data-ttu-id="4da1a-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="4da1a-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4da1a-127">-Porta</span><span class="sxs-lookup"><span data-stu-id="4da1a-127">-Port</span></span>
<span data-ttu-id="4da1a-128">Specifica il numero di porta usato per connettersi a DatabaseHost specificato con queste credenziali.</span><span class="sxs-lookup"><span data-stu-id="4da1a-128">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateByFullURI
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4da1a-129">-Uri</span><span class="sxs-lookup"><span data-stu-id="4da1a-129">-Uri</span></span>
<span data-ttu-id="4da1a-130">Specifica l'URI (Uniform Resource Identifier) completo dell'origine dati esterna a cui queste credenziali possono connettersi.</span><span class="sxs-lookup"><span data-stu-id="4da1a-130">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

```yaml
Type: System.Uri
Parameter Sets: CreateByHostNameAndPort
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4da1a-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4da1a-131">-Confirm</span></span>
<span data-ttu-id="4da1a-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4da1a-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4da1a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4da1a-133">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4da1a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4da1a-134">CommonParameters</span></span>
<span data-ttu-id="4da1a-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4da1a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4da1a-136">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4da1a-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4da1a-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="4da1a-137">INPUTS</span></span>

### <span data-ttu-id="4da1a-138">System.String</span><span class="sxs-lookup"><span data-stu-id="4da1a-138">System.String</span></span>

### <span data-ttu-id="4da1a-139">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="4da1a-139">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="4da1a-140">System.Uri</span><span class="sxs-lookup"><span data-stu-id="4da1a-140">System.Uri</span></span>

### <span data-ttu-id="4da1a-141">System.Int32</span><span class="sxs-lookup"><span data-stu-id="4da1a-141">System.Int32</span></span>

## <span data-ttu-id="4da1a-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4da1a-142">OUTPUTS</span></span>

### <span data-ttu-id="4da1a-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span><span class="sxs-lookup"><span data-stu-id="4da1a-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span></span>

## <span data-ttu-id="4da1a-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="4da1a-144">NOTES</span></span>

## <span data-ttu-id="4da1a-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4da1a-145">RELATED LINKS</span></span>
