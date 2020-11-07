---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: CAB32C72-5C16-467E-BC57-749EC49916BB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogSecret.md
ms.openlocfilehash: e807d1fd1c630554bbaefe0cae1dd225b5f1a184
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687232"
---
# <span data-ttu-id="11cd3-101">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="11cd3-101">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>

## <span data-ttu-id="11cd3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="11cd3-102">SYNOPSIS</span></span>
<span data-ttu-id="11cd3-103">Modifica un segreto del catalogo di analisi dei dati di Lake.</span><span class="sxs-lookup"><span data-stu-id="11cd3-103">Modifies a Data Lake Analytics catalog secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11cd3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="11cd3-104">SYNTAX</span></span>

### <span data-ttu-id="11cd3-105">Specificare l'URI completo</span><span class="sxs-lookup"><span data-stu-id="11cd3-105">Specify full URI</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-DatabaseHost] <String> [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11cd3-106">Specificare il nome host e la porta</span><span class="sxs-lookup"><span data-stu-id="11cd3-106">Specify host name and port</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-Uri] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11cd3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="11cd3-107">DESCRIPTION</span></span>
<span data-ttu-id="11cd3-108">Il cmdlet **set-AzureRmDataLakeAnalyticsCatalogSecret** modifica un segreto associato a un catalogo di dati di analisi di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="11cd3-108">The **Set-AzureRmDataLakeAnalyticsCatalogSecret** cmdlet modifies a secret associated with an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="11cd3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="11cd3-109">EXAMPLES</span></span>

### <span data-ttu-id="11cd3-110">Esempio 1: modificare il segreto associato a un account</span><span class="sxs-lookup"><span data-stu-id="11cd3-110">Example 1: Modify the secret associated with an account</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsCatalogSecret -Account "ContosoAdlAccount" -DatabaseName "databaseName" -Secret (Get-Credential) -Host "https://example.contoso.com" -Port 8080
```

<span data-ttu-id="11cd3-111">Questo comando imposta il segreto associato a un catalogo dati di analisi del lago.</span><span class="sxs-lookup"><span data-stu-id="11cd3-111">This command sets the secret associated with a Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="11cd3-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="11cd3-112">PARAMETERS</span></span>

### <span data-ttu-id="11cd3-113">-Account</span><span class="sxs-lookup"><span data-stu-id="11cd3-113">-Account</span></span>
<span data-ttu-id="11cd3-114">Specifica il nome dell'account analisi dati lago.</span><span class="sxs-lookup"><span data-stu-id="11cd3-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="11cd3-115">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="11cd3-115">-DatabaseHost</span></span>
<span data-ttu-id="11cd3-116">Specifica il nome host per il database a cui è associato il segreto nel formato "mydatabase.contoso.com".</span><span class="sxs-lookup"><span data-stu-id="11cd3-116">Specifies the host name for the database the secret is associated with in the format 'mydatabase.contoso.com'.</span></span>

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

### <span data-ttu-id="11cd3-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="11cd3-117">-DatabaseName</span></span>
<span data-ttu-id="11cd3-118">Specifica il nome del database che contiene il segreto.</span><span class="sxs-lookup"><span data-stu-id="11cd3-118">Specifies the name of the database holding the secret.</span></span>

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

### <span data-ttu-id="11cd3-119">-Porta</span><span class="sxs-lookup"><span data-stu-id="11cd3-119">-Port</span></span>
<span data-ttu-id="11cd3-120">Specifica il numero di porta del segreto.</span><span class="sxs-lookup"><span data-stu-id="11cd3-120">Specifies the port number of the secret.</span></span>

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

### <span data-ttu-id="11cd3-121">-Segreto</span><span class="sxs-lookup"><span data-stu-id="11cd3-121">-Secret</span></span>
<span data-ttu-id="11cd3-122">Specifica il nome e la password del segreto.</span><span class="sxs-lookup"><span data-stu-id="11cd3-122">Specifies the name and password of the secret.</span></span>

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

### <span data-ttu-id="11cd3-123">-URI</span><span class="sxs-lookup"><span data-stu-id="11cd3-123">-Uri</span></span>
<span data-ttu-id="11cd3-124">Specifica l'URI (Uniform Resource Identifier) per il segreto.</span><span class="sxs-lookup"><span data-stu-id="11cd3-124">Specifies the Uniform Resource Identifier (URI) for the secret.</span></span>

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

### <span data-ttu-id="11cd3-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11cd3-125">-DefaultProfile</span></span>
<span data-ttu-id="11cd3-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="11cd3-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11cd3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11cd3-127">CommonParameters</span></span>
<span data-ttu-id="11cd3-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11cd3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11cd3-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11cd3-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11cd3-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="11cd3-130">INPUTS</span></span>

## <span data-ttu-id="11cd3-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="11cd3-131">OUTPUTS</span></span>

### <span data-ttu-id="11cd3-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="11cd3-132">None</span></span>

## <span data-ttu-id="11cd3-133">Note</span><span class="sxs-lookup"><span data-stu-id="11cd3-133">NOTES</span></span>

## <span data-ttu-id="11cd3-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="11cd3-134">RELATED LINKS</span></span>

[<span data-ttu-id="11cd3-135">New-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="11cd3-135">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./New-AzureRmDataLakeAnalyticsCatalogSecret.md)

[<span data-ttu-id="11cd3-136">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="11cd3-136">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Remove-AzureRmDataLakeAnalyticsCatalogSecret.md)


