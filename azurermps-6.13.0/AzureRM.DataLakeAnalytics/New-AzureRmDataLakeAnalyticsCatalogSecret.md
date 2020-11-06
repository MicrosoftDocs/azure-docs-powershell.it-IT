---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: C0BE6C8D-37F5-445F-AE15-2CD4F8D8E031
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/new-azurermdatalakeanalyticscatalogsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogSecret.md
ms.openlocfilehash: ce6bd748a639116f1f6d2e5c42e824fb3687bdfb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520224"
---
# <span data-ttu-id="71497-101">New-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="71497-101">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>

## <span data-ttu-id="71497-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="71497-102">SYNOPSIS</span></span>
<span data-ttu-id="71497-103">Crea un segreto del catalogo dei dati di Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="71497-103">Creates a Data Lake Analytics catalog secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71497-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="71497-104">SYNTAX</span></span>

### <span data-ttu-id="71497-105">CreateByFullURI</span><span class="sxs-lookup"><span data-stu-id="71497-105">CreateByFullURI</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-DatabaseHost] <String> [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71497-106">CreateByHostNameAndPort</span><span class="sxs-lookup"><span data-stu-id="71497-106">CreateByHostNameAndPort</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-Uri] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71497-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71497-107">DESCRIPTION</span></span>
<span data-ttu-id="71497-108">Il cmdlet **New-AzureRmDataLakeAnalyticsCatalogSecret** crea un segreto da usare in un catalogo di dati di analisi di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="71497-108">The **New-AzureRmDataLakeAnalyticsCatalogSecret** cmdlet creates a secret to use in an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="71497-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="71497-109">EXAMPLES</span></span>

### <span data-ttu-id="71497-110">Esempio 1: ottenere il segreto per un catalogo</span><span class="sxs-lookup"><span data-stu-id="71497-110">Example 1: Get the secret for a catalog</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsCatalogSecret -Account "ContosoAdlAccount" -DatabaseName "databaseName" -Secret (Get-Credential) -Host "https://example.contoso.com" -Port 8080
```

<span data-ttu-id="71497-111">Questo comando ottiene il segreto corrispondente all'account, al database, alle credenziali e all'host specificati.</span><span class="sxs-lookup"><span data-stu-id="71497-111">This command gets the secret corresponding to the specified account, database, credential, and host.</span></span>

## <span data-ttu-id="71497-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="71497-112">PARAMETERS</span></span>

### <span data-ttu-id="71497-113">-Account</span><span class="sxs-lookup"><span data-stu-id="71497-113">-Account</span></span>
<span data-ttu-id="71497-114">Specifica il nome dell'account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="71497-114">Specifies the name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="71497-115">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="71497-115">-DatabaseHost</span></span>
<span data-ttu-id="71497-116">Specifica il nome host per il database a cui è associato il segreto nel formato "mydatabase.contoso.com".</span><span class="sxs-lookup"><span data-stu-id="71497-116">Specifies the host name for the database the secret is associated with in the format 'mydatabase.contoso.com'.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByFullURI
Aliases: Host

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71497-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="71497-117">-DatabaseName</span></span>
<span data-ttu-id="71497-118">Specifica il nome del database che contiene il segreto.</span><span class="sxs-lookup"><span data-stu-id="71497-118">Specifies the name of the database that holds the secret.</span></span>

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

### <span data-ttu-id="71497-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71497-119">-DefaultProfile</span></span>
<span data-ttu-id="71497-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="71497-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71497-121">-Porta</span><span class="sxs-lookup"><span data-stu-id="71497-121">-Port</span></span>
<span data-ttu-id="71497-122">Specifica il numero di porta del segreto.</span><span class="sxs-lookup"><span data-stu-id="71497-122">Specifies the port number of the secret.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateByFullURI
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71497-123">-Segreto</span><span class="sxs-lookup"><span data-stu-id="71497-123">-Secret</span></span>
<span data-ttu-id="71497-124">Specifica il nome e la password del segreto.</span><span class="sxs-lookup"><span data-stu-id="71497-124">Specifies the name and password of the secret.</span></span>

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

### <span data-ttu-id="71497-125">-URI</span><span class="sxs-lookup"><span data-stu-id="71497-125">-Uri</span></span>
<span data-ttu-id="71497-126">Specifica l'URI (Uniform Resource Identifier) del segreto.</span><span class="sxs-lookup"><span data-stu-id="71497-126">Specifies the Uniform Resource Identifier (URI) of the secret.</span></span>

```yaml
Type: System.Uri
Parameter Sets: CreateByHostNameAndPort
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71497-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71497-127">CommonParameters</span></span>
<span data-ttu-id="71497-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71497-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71497-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71497-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71497-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="71497-130">INPUTS</span></span>

### <span data-ttu-id="71497-131">System. String</span><span class="sxs-lookup"><span data-stu-id="71497-131">System.String</span></span>

### <span data-ttu-id="71497-132">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="71497-132">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="71497-133">System. Uri</span><span class="sxs-lookup"><span data-stu-id="71497-133">System.Uri</span></span>

### <span data-ttu-id="71497-134">System. Int32</span><span class="sxs-lookup"><span data-stu-id="71497-134">System.Int32</span></span>

## <span data-ttu-id="71497-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="71497-135">OUTPUTS</span></span>

### <span data-ttu-id="71497-136">Microsoft. Azure. Management. datalake. Analytics. Models. USqlSecret</span><span class="sxs-lookup"><span data-stu-id="71497-136">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlSecret</span></span>

## <span data-ttu-id="71497-137">Note</span><span class="sxs-lookup"><span data-stu-id="71497-137">NOTES</span></span>

## <span data-ttu-id="71497-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="71497-138">RELATED LINKS</span></span>

[<span data-ttu-id="71497-139">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="71497-139">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Remove-AzureRmDataLakeAnalyticsCatalogSecret.md)

[<span data-ttu-id="71497-140">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="71497-140">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Set-AzureRmDataLakeAnalyticsCatalogSecret.md)


