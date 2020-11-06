---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 22ACB910-0C41-4649-8D22-537E38CB4570
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappdatabasebackupsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppDatabaseBackupSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppDatabaseBackupSetting.md
ms.openlocfilehash: 7eea25d4b82dc8a424fea0cbd3e361014c77c396
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519323"
---
# <span data-ttu-id="82827-101">New-AzureRmWebAppDatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="82827-101">New-AzureRmWebAppDatabaseBackupSetting</span></span>

## <span data-ttu-id="82827-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="82827-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82827-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="82827-103">SYNTAX</span></span>

```
New-AzureRmWebAppDatabaseBackupSetting [-Name] <String> [-DatabaseType] <String> [-ConnectionString] <String>
 [[-ConnectionStringName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82827-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82827-104">DESCRIPTION</span></span>
<span data-ttu-id="82827-105">Il cmdlet **New-AzureRmWebAppDatabaseBackupSetting** crea una nuova impostazione di backup di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="82827-105">The **New-AzureRmWebAppDatabaseBackupSetting** cmdlet creates a new Azure Web App Backup setting.</span></span>

## <span data-ttu-id="82827-106">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="82827-106">EXAMPLES</span></span>

### <span data-ttu-id="82827-107">1:</span><span class="sxs-lookup"><span data-stu-id="82827-107">1:</span></span>
```
PS C:\> New-AzureRmWebAppDatabaseBackupSetting -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -ConnectionString "MyConnectionString" -DatabaseType "SqlAzure"
```

<span data-ttu-id="82827-108">Crea un'impostazione di backup del database (stringa di connessione) di tipo sqlazure per l'app specificata ContosoWebApp che si trova all'interno del gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="82827-108">Creates a database backup setting (connection string) of type SqlAzure for the specified app ContosoWebApp that is within resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="82827-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="82827-109">PARAMETERS</span></span>

### <span data-ttu-id="82827-110">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="82827-110">-ConnectionString</span></span>
<span data-ttu-id="82827-111">Stringa di connessione</span><span class="sxs-lookup"><span data-stu-id="82827-111">Connection String</span></span>

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

### <span data-ttu-id="82827-112">-ConnectionStringname</span><span class="sxs-lookup"><span data-stu-id="82827-112">-ConnectionStringName</span></span>
<span data-ttu-id="82827-113">Nome stringa di connessione</span><span class="sxs-lookup"><span data-stu-id="82827-113">Connection String Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82827-114">-DatabaseType</span><span class="sxs-lookup"><span data-stu-id="82827-114">-DatabaseType</span></span>
<span data-ttu-id="82827-115">Tipo di database (ad esempio "sqlazure" o "MySql")</span><span class="sxs-lookup"><span data-stu-id="82827-115">Database Type ( e.g. "SqlAzure" or "MySql" )</span></span>

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

### <span data-ttu-id="82827-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82827-116">-DefaultProfile</span></span>
<span data-ttu-id="82827-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="82827-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82827-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="82827-118">-Name</span></span>
<span data-ttu-id="82827-119">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="82827-119">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82827-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82827-120">CommonParameters</span></span>
<span data-ttu-id="82827-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82827-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82827-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82827-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82827-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="82827-123">INPUTS</span></span>

### <span data-ttu-id="82827-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="82827-124">None</span></span>
<span data-ttu-id="82827-125">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="82827-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="82827-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="82827-126">OUTPUTS</span></span>

### <span data-ttu-id="82827-127">Microsoft. Azure. Management. website. Models. DatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="82827-127">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting</span></span>

## <span data-ttu-id="82827-128">Note</span><span class="sxs-lookup"><span data-stu-id="82827-128">NOTES</span></span>

## <span data-ttu-id="82827-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="82827-129">RELATED LINKS</span></span>

