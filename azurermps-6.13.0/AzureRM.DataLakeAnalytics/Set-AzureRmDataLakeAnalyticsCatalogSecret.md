---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: CAB32C72-5C16-467E-BC57-749EC49916BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/set-azurermdatalakeanalyticscatalogsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogSecret.md
ms.openlocfilehash: 22a10d4f65d43f4d11871cbf43399bfc35febf04
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520644"
---
# <span data-ttu-id="d7edc-101">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="d7edc-101">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>

## <span data-ttu-id="d7edc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d7edc-102">SYNOPSIS</span></span>
<span data-ttu-id="d7edc-103">Modifica un segreto del catalogo di analisi dei dati di Lake.</span><span class="sxs-lookup"><span data-stu-id="d7edc-103">Modifies a Data Lake Analytics catalog secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7edc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d7edc-104">SYNTAX</span></span>

### <span data-ttu-id="d7edc-105">SetByFullUri</span><span class="sxs-lookup"><span data-stu-id="d7edc-105">SetByFullUri</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-DatabaseHost] <String> [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7edc-106">SetByHostNameAndPort</span><span class="sxs-lookup"><span data-stu-id="d7edc-106">SetByHostNameAndPort</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-Uri] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7edc-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d7edc-107">DESCRIPTION</span></span>
<span data-ttu-id="d7edc-108">Il cmdlet **set-AzureRmDataLakeAnalyticsCatalogSecret** modifica un segreto associato a un catalogo di dati di analisi di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="d7edc-108">The **Set-AzureRmDataLakeAnalyticsCatalogSecret** cmdlet modifies a secret associated with an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="d7edc-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d7edc-109">EXAMPLES</span></span>

### <span data-ttu-id="d7edc-110">Esempio 1: modificare il segreto associato a un account</span><span class="sxs-lookup"><span data-stu-id="d7edc-110">Example 1: Modify the secret associated with an account</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsCatalogSecret -Account "ContosoAdlAccount" -DatabaseName "databaseName" -Secret (Get-Credential) -Host "https://example.contoso.com" -Port 8080
```

<span data-ttu-id="d7edc-111">Questo comando imposta il segreto associato a un catalogo dati di analisi del lago.</span><span class="sxs-lookup"><span data-stu-id="d7edc-111">This command sets the secret associated with a Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="d7edc-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d7edc-112">PARAMETERS</span></span>

### <span data-ttu-id="d7edc-113">-Account</span><span class="sxs-lookup"><span data-stu-id="d7edc-113">-Account</span></span>
<span data-ttu-id="d7edc-114">Specifica il nome dell'account analisi dati lago.</span><span class="sxs-lookup"><span data-stu-id="d7edc-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="d7edc-115">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="d7edc-115">-DatabaseHost</span></span>
<span data-ttu-id="d7edc-116">Specifica il nome host per il database a cui è associato il segreto nel formato "mydatabase.contoso.com".</span><span class="sxs-lookup"><span data-stu-id="d7edc-116">Specifies the host name for the database the secret is associated with in the format 'mydatabase.contoso.com'.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByFullUri
Aliases: Host

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7edc-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d7edc-117">-DatabaseName</span></span>
<span data-ttu-id="d7edc-118">Specifica il nome del database che contiene il segreto.</span><span class="sxs-lookup"><span data-stu-id="d7edc-118">Specifies the name of the database holding the secret.</span></span>

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

### <span data-ttu-id="d7edc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7edc-119">-DefaultProfile</span></span>
<span data-ttu-id="d7edc-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d7edc-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d7edc-121">-Porta</span><span class="sxs-lookup"><span data-stu-id="d7edc-121">-Port</span></span>
<span data-ttu-id="d7edc-122">Specifica il numero di porta del segreto.</span><span class="sxs-lookup"><span data-stu-id="d7edc-122">Specifies the port number of the secret.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByFullUri
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7edc-123">-Segreto</span><span class="sxs-lookup"><span data-stu-id="d7edc-123">-Secret</span></span>
<span data-ttu-id="d7edc-124">Specifica il nome e la password del segreto.</span><span class="sxs-lookup"><span data-stu-id="d7edc-124">Specifies the name and password of the secret.</span></span>

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

### <span data-ttu-id="d7edc-125">-URI</span><span class="sxs-lookup"><span data-stu-id="d7edc-125">-Uri</span></span>
<span data-ttu-id="d7edc-126">Specifica l'URI (Uniform Resource Identifier) per il segreto.</span><span class="sxs-lookup"><span data-stu-id="d7edc-126">Specifies the Uniform Resource Identifier (URI) for the secret.</span></span>

```yaml
Type: System.Uri
Parameter Sets: SetByHostNameAndPort
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7edc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7edc-127">CommonParameters</span></span>
<span data-ttu-id="d7edc-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7edc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7edc-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7edc-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7edc-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d7edc-130">INPUTS</span></span>

### <span data-ttu-id="d7edc-131">System. String</span><span class="sxs-lookup"><span data-stu-id="d7edc-131">System.String</span></span>

### <span data-ttu-id="d7edc-132">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="d7edc-132">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="d7edc-133">System. Uri</span><span class="sxs-lookup"><span data-stu-id="d7edc-133">System.Uri</span></span>

### <span data-ttu-id="d7edc-134">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d7edc-134">System.Int32</span></span>

## <span data-ttu-id="d7edc-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d7edc-135">OUTPUTS</span></span>

### <span data-ttu-id="d7edc-136">Microsoft. Azure. Management. datalake. Analytics. Models. USqlSecret</span><span class="sxs-lookup"><span data-stu-id="d7edc-136">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlSecret</span></span>

## <span data-ttu-id="d7edc-137">Note</span><span class="sxs-lookup"><span data-stu-id="d7edc-137">NOTES</span></span>

## <span data-ttu-id="d7edc-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d7edc-138">RELATED LINKS</span></span>

[<span data-ttu-id="d7edc-139">New-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="d7edc-139">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./New-AzureRmDataLakeAnalyticsCatalogSecret.md)

[<span data-ttu-id="d7edc-140">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="d7edc-140">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Remove-AzureRmDataLakeAnalyticsCatalogSecret.md)


