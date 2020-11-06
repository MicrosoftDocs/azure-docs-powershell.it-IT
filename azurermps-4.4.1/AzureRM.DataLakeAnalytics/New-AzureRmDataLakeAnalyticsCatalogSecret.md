---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: C0BE6C8D-37F5-445F-AE15-2CD4F8D8E031
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogSecret.md
ms.openlocfilehash: e36030cbe1ccfe78db625d9d4142de13ba2f54ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510668"
---
# <span data-ttu-id="76996-101">New-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="76996-101">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>

## <span data-ttu-id="76996-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="76996-102">SYNOPSIS</span></span>
<span data-ttu-id="76996-103">Crea un segreto del catalogo dei dati di Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="76996-103">Creates a Data Lake Analytics catalog secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76996-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="76996-104">SYNTAX</span></span>

### <span data-ttu-id="76996-105">Specificare l'URI completo</span><span class="sxs-lookup"><span data-stu-id="76996-105">Specify full URI</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-DatabaseHost] <String> [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76996-106">Specificare il nome host e la porta</span><span class="sxs-lookup"><span data-stu-id="76996-106">Specify host name and port</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-Uri] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76996-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="76996-107">DESCRIPTION</span></span>
<span data-ttu-id="76996-108">Il cmdlet **New-AzureRmDataLakeAnalyticsCatalogSecret** crea un segreto da usare in un catalogo di dati di analisi di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="76996-108">The **New-AzureRmDataLakeAnalyticsCatalogSecret** cmdlet creates a secret to use in an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="76996-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="76996-109">EXAMPLES</span></span>

### <span data-ttu-id="76996-110">Esempio 1: ottenere il segreto per un catalogo</span><span class="sxs-lookup"><span data-stu-id="76996-110">Example 1: Get the secret for a catalog</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsCatalogSecret -Account "ContosoAdlAccount" -DatabaseName "databaseName" -Secret (Get-Credential) -Host "https://example.contoso.com" -Port 8080
```

<span data-ttu-id="76996-111">Questo comando ottiene il segreto corrispondente all'account, al database, alle credenziali e all'host specificati.</span><span class="sxs-lookup"><span data-stu-id="76996-111">This command gets the secret corresponding to the specified account, database, credential, and host.</span></span>

## <span data-ttu-id="76996-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="76996-112">PARAMETERS</span></span>

### <span data-ttu-id="76996-113">-Account</span><span class="sxs-lookup"><span data-stu-id="76996-113">-Account</span></span>
<span data-ttu-id="76996-114">Specifica il nome dell'account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="76996-114">Specifies the name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="76996-115">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="76996-115">-DatabaseHost</span></span>
<span data-ttu-id="76996-116">Specifica il nome host per il database a cui è associato il segreto nel formato "mydatabase.contoso.com".</span><span class="sxs-lookup"><span data-stu-id="76996-116">Specifies the host name for the database the secret is associated with in the format 'mydatabase.contoso.com'.</span></span>

```yaml
Type: System.String
Parameter Sets: Specify full URI
Aliases: Host

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76996-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="76996-117">-DatabaseName</span></span>
<span data-ttu-id="76996-118">Specifica il nome del database che contiene il segreto.</span><span class="sxs-lookup"><span data-stu-id="76996-118">Specifies the name of the database that holds the secret.</span></span>

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

### <span data-ttu-id="76996-119">-Porta</span><span class="sxs-lookup"><span data-stu-id="76996-119">-Port</span></span>
<span data-ttu-id="76996-120">Specifica il numero di porta del segreto.</span><span class="sxs-lookup"><span data-stu-id="76996-120">Specifies the port number of the secret.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Specify full URI
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76996-121">-Segreto</span><span class="sxs-lookup"><span data-stu-id="76996-121">-Secret</span></span>
<span data-ttu-id="76996-122">Specifica il nome e la password del segreto.</span><span class="sxs-lookup"><span data-stu-id="76996-122">Specifies the name and password of the secret.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76996-123">-URI</span><span class="sxs-lookup"><span data-stu-id="76996-123">-Uri</span></span>
<span data-ttu-id="76996-124">Specifica l'URI (Uniform Resource Identifier) del segreto.</span><span class="sxs-lookup"><span data-stu-id="76996-124">Specifies the Uniform Resource Identifier (URI) of the secret.</span></span>

```yaml
Type: System.Uri
Parameter Sets: Specify host name and port
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76996-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76996-125">-DefaultProfile</span></span>
<span data-ttu-id="76996-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="76996-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76996-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76996-127">CommonParameters</span></span>
<span data-ttu-id="76996-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76996-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76996-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76996-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76996-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="76996-130">INPUTS</span></span>

## <span data-ttu-id="76996-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="76996-131">OUTPUTS</span></span>

### <span data-ttu-id="76996-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="76996-132">None</span></span>

## <span data-ttu-id="76996-133">Note</span><span class="sxs-lookup"><span data-stu-id="76996-133">NOTES</span></span>

## <span data-ttu-id="76996-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="76996-134">RELATED LINKS</span></span>

[<span data-ttu-id="76996-135">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="76996-135">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Remove-AzureRmDataLakeAnalyticsCatalogSecret.md)

[<span data-ttu-id="76996-136">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="76996-136">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Set-AzureRmDataLakeAnalyticsCatalogSecret.md)


