---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 22ACB910-0C41-4649-8D22-537E38CB4570
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappdatabasebackupsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppDatabaseBackupSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppDatabaseBackupSetting.md
ms.openlocfilehash: 480532e2fffcc2b03a57c7d0a63cc2737844f652
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018691"
---
# <span data-ttu-id="fb4ee-101">New-AzWebAppDatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="fb4ee-101">New-AzWebAppDatabaseBackupSetting</span></span>

## <span data-ttu-id="fb4ee-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fb4ee-102">SYNOPSIS</span></span>

## <span data-ttu-id="fb4ee-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fb4ee-103">SYNTAX</span></span>

```
New-AzWebAppDatabaseBackupSetting [-Name] <String> [-DatabaseType] <String> [-ConnectionString] <String>
 [[-ConnectionStringName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb4ee-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fb4ee-104">DESCRIPTION</span></span>
<span data-ttu-id="fb4ee-105">Il cmdlet **New-AzWebAppDatabaseBackupSetting** crea una nuova impostazione di backup di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="fb4ee-105">The **New-AzWebAppDatabaseBackupSetting** cmdlet creates a new Azure Web App Backup setting.</span></span>

## <span data-ttu-id="fb4ee-106">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fb4ee-106">EXAMPLES</span></span>

### <span data-ttu-id="fb4ee-107">1:</span><span class="sxs-lookup"><span data-stu-id="fb4ee-107">1:</span></span>
```
PS C:\> New-AzWebAppDatabaseBackupSetting -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -ConnectionString "MyConnectionString" -DatabaseType "SqlAzure"
```

<span data-ttu-id="fb4ee-108">Crea un'impostazione di backup del database (stringa di connessione) di tipo sqlazure per l'app specificata ContosoWebApp che si trova all'interno del gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="fb4ee-108">Creates a database backup setting (connection string) of type SqlAzure for the specified app ContosoWebApp that is within resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="fb4ee-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fb4ee-109">PARAMETERS</span></span>

### <span data-ttu-id="fb4ee-110">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="fb4ee-110">-ConnectionString</span></span>
<span data-ttu-id="fb4ee-111">Stringa di connessione</span><span class="sxs-lookup"><span data-stu-id="fb4ee-111">Connection String</span></span>

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

### <span data-ttu-id="fb4ee-112">-ConnectionStringname</span><span class="sxs-lookup"><span data-stu-id="fb4ee-112">-ConnectionStringName</span></span>
<span data-ttu-id="fb4ee-113">Nome stringa di connessione</span><span class="sxs-lookup"><span data-stu-id="fb4ee-113">Connection String Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb4ee-114">-DatabaseType</span><span class="sxs-lookup"><span data-stu-id="fb4ee-114">-DatabaseType</span></span>
<span data-ttu-id="fb4ee-115">Tipo di database (ad esempio "sqlazure" o "MySql")</span><span class="sxs-lookup"><span data-stu-id="fb4ee-115">Database Type ( e.g. "SqlAzure" or "MySql" )</span></span>

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

### <span data-ttu-id="fb4ee-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb4ee-116">-DefaultProfile</span></span>
<span data-ttu-id="fb4ee-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fb4ee-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb4ee-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="fb4ee-118">-Name</span></span>
<span data-ttu-id="fb4ee-119">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="fb4ee-119">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb4ee-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb4ee-120">CommonParameters</span></span>
<span data-ttu-id="fb4ee-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb4ee-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb4ee-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb4ee-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb4ee-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fb4ee-123">INPUTS</span></span>

### <span data-ttu-id="fb4ee-124">System. String</span><span class="sxs-lookup"><span data-stu-id="fb4ee-124">System.String</span></span>

## <span data-ttu-id="fb4ee-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fb4ee-125">OUTPUTS</span></span>

### <span data-ttu-id="fb4ee-126">Microsoft. Azure. Management. website. Models. DatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="fb4ee-126">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting</span></span>

## <span data-ttu-id="fb4ee-127">Note</span><span class="sxs-lookup"><span data-stu-id="fb4ee-127">NOTES</span></span>

## <span data-ttu-id="fb4ee-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fb4ee-128">RELATED LINKS</span></span>
