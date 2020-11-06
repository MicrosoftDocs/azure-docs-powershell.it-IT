---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: BB6AF5A9-49BD-4A76-9F3F-44B62D2AB842
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/new-azurermdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 2dd97b310de764638fab029c60407c578287e9a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512655"
---
# <span data-ttu-id="a5064-101">New-AzureRmDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="a5064-101">New-AzureRmDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="a5064-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a5064-102">SYNOPSIS</span></span>
<span data-ttu-id="a5064-103">Crea una nuova credenziale del catalogo di analisi del Lago di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="a5064-103">Creates a new Azure Data Lake Analytics catalog credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5064-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a5064-104">SYNTAX</span></span>

### <span data-ttu-id="a5064-105">CreateByHostNameAndPort (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a5064-105">CreateByHostNameAndPort (Default)</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5064-106">CreateByFullURI</span><span class="sxs-lookup"><span data-stu-id="a5064-106">CreateByFullURI</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-DatabaseHost] <String> [-Port] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5064-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a5064-107">DESCRIPTION</span></span>
<span data-ttu-id="a5064-108">Il cmdlet New-AzureRmDataLakeAnalyticsCatalogCredential crea una nuova credenziale da usare in un catalogo di dati di analisi di Azure Data Lake per la connessione a origini dati esterne.</span><span class="sxs-lookup"><span data-stu-id="a5064-108">The New-AzureRmDataLakeAnalyticsCatalogCredential cmdlet creates a new credential to use in an Azure Data Lake Analytics catalog for connecting to external data sources.</span></span>

## <span data-ttu-id="a5064-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a5064-109">EXAMPLES</span></span>

### <span data-ttu-id="a5064-110">Esempio 1: creare una credenziale per un catalogo che specifica l'host e la porta</span><span class="sxs-lookup"><span data-stu-id="a5064-110">Example 1: Create a credential for a catalog specifying host and port</span></span>
```
PS C:\> New-AzureRmDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -DatabaseHost "example.contoso.com" -Port 8080
```

<span data-ttu-id="a5064-111">Questo comando crea le credenziali specificate per l'account, il database, l'host e la porta specificati usando il protocollo HTTPS.</span><span class="sxs-lookup"><span data-stu-id="a5064-111">This command creates the specified credential for the specified account, database, host and port using https protocol.</span></span>

### <span data-ttu-id="a5064-112">Esempio 2: creare una credenziale per un catalogo che specifica l'URI completo</span><span class="sxs-lookup"><span data-stu-id="a5064-112">Example 2: Create a credential for a catalog specifying full URI</span></span>
```
PS C:\> New-AzureRmDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -Uri "http://httpExample.contoso.com:8080"
```

<span data-ttu-id="a5064-113">Questo comando crea le credenziali specificate per l'account, il database e l'URI dell'origine dati esterni specificati.</span><span class="sxs-lookup"><span data-stu-id="a5064-113">This command creates the specified credential for the specified account, database and external data source URI.</span></span>

## <span data-ttu-id="a5064-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a5064-114">PARAMETERS</span></span>

### <span data-ttu-id="a5064-115">-Account</span><span class="sxs-lookup"><span data-stu-id="a5064-115">-Account</span></span>
<span data-ttu-id="a5064-116">Specifica il nome dell'account analisi dati lago.</span><span class="sxs-lookup"><span data-stu-id="a5064-116">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5064-117">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="a5064-117">-Credential</span></span>
<span data-ttu-id="a5064-118">Specifica il nome utente e la password corrispondente della credenziale.</span><span class="sxs-lookup"><span data-stu-id="a5064-118">Specifies the user name and corresponding password of the credential.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5064-119">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="a5064-119">-CredentialName</span></span>
<span data-ttu-id="a5064-120">Specifica il nome e la password della credenziale.</span><span class="sxs-lookup"><span data-stu-id="a5064-120">Specifies the name and password of the credential.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5064-121">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="a5064-121">-DatabaseHost</span></span>
<span data-ttu-id="a5064-122">Specifica il nome host dell'origine dati esterna a cui può connettersi la credenziale in formato mydatabase.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="a5064-122">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

```yaml
Type: String
Parameter Sets: CreateByFullURI
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5064-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a5064-123">-DatabaseName</span></span>
<span data-ttu-id="a5064-124">Specifica il nome del database nel acocunt di analisi dei dati del lago in cui verranno archiviate le credenziali.</span><span class="sxs-lookup"><span data-stu-id="a5064-124">Specifies the name of the database in the Data Lake Analytics acocunt that the credential will be stored in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5064-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5064-125">-DefaultProfile</span></span>
<span data-ttu-id="a5064-126">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a5064-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5064-127">-Porta</span><span class="sxs-lookup"><span data-stu-id="a5064-127">-Port</span></span>
<span data-ttu-id="a5064-128">Specifica il numero di porta usato per connettersi al DatabaseHost specificato usando questa credenziale.</span><span class="sxs-lookup"><span data-stu-id="a5064-128">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

```yaml
Type: Int32
Parameter Sets: CreateByFullURI
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5064-129">-URI</span><span class="sxs-lookup"><span data-stu-id="a5064-129">-Uri</span></span>
<span data-ttu-id="a5064-130">Specifica l'URI (Uniform Resource Identifier) completo dell'origine dati esterna a cui può connettersi la credenziale.</span><span class="sxs-lookup"><span data-stu-id="a5064-130">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

```yaml
Type: Uri
Parameter Sets: CreateByHostNameAndPort
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5064-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a5064-131">-Confirm</span></span>
<span data-ttu-id="a5064-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5064-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5064-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5064-133">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5064-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5064-134">CommonParameters</span></span>
<span data-ttu-id="a5064-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5064-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5064-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5064-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5064-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a5064-137">INPUTS</span></span>

### <span data-ttu-id="a5064-138">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a5064-138">None</span></span>
<span data-ttu-id="a5064-139">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="a5064-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a5064-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a5064-140">OUTPUTS</span></span>

### <span data-ttu-id="a5064-141">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a5064-141">None</span></span>

## <span data-ttu-id="a5064-142">Note</span><span class="sxs-lookup"><span data-stu-id="a5064-142">NOTES</span></span>

## <span data-ttu-id="a5064-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a5064-143">RELATED LINKS</span></span>
