---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: BB6AF5A9-49BD-4A76-9F3F-44B62D2AB842
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 1668ca10c8c3425bea7c4082033abb19f8de7306
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510672"
---
# <span data-ttu-id="c55ef-101">New-AzureRmDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="c55ef-101">New-AzureRmDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="c55ef-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c55ef-102">SYNOPSIS</span></span>
<span data-ttu-id="c55ef-103">Crea una nuova credenziale del catalogo di analisi del Lago di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="c55ef-103">Creates a new Azure Data Lake Analytics catalog credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c55ef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c55ef-104">SYNTAX</span></span>

### <span data-ttu-id="c55ef-105">Specificare il nome host e la porta (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c55ef-105">Specify host name and port (Default)</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c55ef-106">Specificare l'URI completo</span><span class="sxs-lookup"><span data-stu-id="c55ef-106">Specify full URI</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-DatabaseHost] <String> [-Port] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c55ef-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c55ef-107">DESCRIPTION</span></span>
<span data-ttu-id="c55ef-108">Il cmdlet New-AzureRmDataLakeAnalyticsCatalogCredential crea una nuova credenziale da usare in un catalogo di dati di analisi di Azure Data Lake per la connessione a origini dati esterne.</span><span class="sxs-lookup"><span data-stu-id="c55ef-108">The New-AzureRmDataLakeAnalyticsCatalogCredential cmdlet creates a new credential to use in an Azure Data Lake Analytics catalog for connecting to external data sources.</span></span>

## <span data-ttu-id="c55ef-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c55ef-109">EXAMPLES</span></span>

### <span data-ttu-id="c55ef-110">Esempio 1: creare una credenziale per un catalogo che specifica l'host e la porta</span><span class="sxs-lookup"><span data-stu-id="c55ef-110">Example 1: Create a credential for a catalog specifying host and port</span></span>
```
PS C:\> New-AzureRmDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -DatabaseHost "example.contoso.com" -Port 8080
```

<span data-ttu-id="c55ef-111">Questo comando crea le credenziali specificate per l'account, il database, l'host e la porta specificati usando il protocollo HTTPS.</span><span class="sxs-lookup"><span data-stu-id="c55ef-111">This command creates the specified credential for the specified account, database, host and port using https protocol.</span></span>

### <span data-ttu-id="c55ef-112">Esempio 2: creare una credenziale per un catalogo che specifica l'URI completo</span><span class="sxs-lookup"><span data-stu-id="c55ef-112">Example 2: Create a credential for a catalog specifying full URI</span></span>
```
PS C:\> New-AzureRmDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -Uri "http://httpExample.contoso.com:8080"
```

<span data-ttu-id="c55ef-113">Questo comando crea le credenziali specificate per l'account, il database e l'URI dell'origine dati esterni specificati.</span><span class="sxs-lookup"><span data-stu-id="c55ef-113">This command creates the specified credential for the specified account, database and external data source URI.</span></span>

## <span data-ttu-id="c55ef-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c55ef-114">PARAMETERS</span></span>

### <span data-ttu-id="c55ef-115">-Account</span><span class="sxs-lookup"><span data-stu-id="c55ef-115">-Account</span></span>
<span data-ttu-id="c55ef-116">Specifica il nome dell'account analisi dati lago.</span><span class="sxs-lookup"><span data-stu-id="c55ef-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="c55ef-117">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="c55ef-117">-Credential</span></span>
<span data-ttu-id="c55ef-118">Specifica il nome utente e la password corrispondente della credenziale.</span><span class="sxs-lookup"><span data-stu-id="c55ef-118">Specifies the user name and corresponding password of the credential.</span></span>

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

### <span data-ttu-id="c55ef-119">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="c55ef-119">-CredentialName</span></span>
<span data-ttu-id="c55ef-120">Specifica il nome e la password della credenziale.</span><span class="sxs-lookup"><span data-stu-id="c55ef-120">Specifies the name and password of the credential.</span></span>

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

### <span data-ttu-id="c55ef-121">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="c55ef-121">-DatabaseHost</span></span>
<span data-ttu-id="c55ef-122">Specifica il nome host dell'origine dati esterna a cui può connettersi la credenziale in formato mydatabase.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="c55ef-122">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

```yaml
Type: System.String
Parameter Sets: Specify full URI
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c55ef-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c55ef-123">-DatabaseName</span></span>
<span data-ttu-id="c55ef-124">Specifica il nome del database nel acocunt di analisi dei dati del lago in cui verranno archiviate le credenziali.</span><span class="sxs-lookup"><span data-stu-id="c55ef-124">Specifies the name of the database in the Data Lake Analytics acocunt that the credential will be stored in.</span></span>

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

### <span data-ttu-id="c55ef-125">-Porta</span><span class="sxs-lookup"><span data-stu-id="c55ef-125">-Port</span></span>
<span data-ttu-id="c55ef-126">Specifica il numero di porta usato per connettersi al DatabaseHost specificato usando questa credenziale.</span><span class="sxs-lookup"><span data-stu-id="c55ef-126">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Specify full URI
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c55ef-127">-URI</span><span class="sxs-lookup"><span data-stu-id="c55ef-127">-Uri</span></span>
<span data-ttu-id="c55ef-128">Specifica l'URI (Uniform Resource Identifier) completo dell'origine dati esterna a cui può connettersi la credenziale.</span><span class="sxs-lookup"><span data-stu-id="c55ef-128">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

```yaml
Type: System.Uri
Parameter Sets: Specify host name and port
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c55ef-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c55ef-129">-Confirm</span></span>
<span data-ttu-id="c55ef-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c55ef-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c55ef-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c55ef-131">-WhatIf</span></span>
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

### <span data-ttu-id="c55ef-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c55ef-132">-DefaultProfile</span></span>
<span data-ttu-id="c55ef-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c55ef-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c55ef-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c55ef-134">CommonParameters</span></span>
<span data-ttu-id="c55ef-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c55ef-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c55ef-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c55ef-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c55ef-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c55ef-137">INPUTS</span></span>

## <span data-ttu-id="c55ef-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c55ef-138">OUTPUTS</span></span>

### <span data-ttu-id="c55ef-139">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c55ef-139">None</span></span>

## <span data-ttu-id="c55ef-140">Note</span><span class="sxs-lookup"><span data-stu-id="c55ef-140">NOTES</span></span>

## <span data-ttu-id="c55ef-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c55ef-141">RELATED LINKS</span></span>

