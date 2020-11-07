---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 22ACB910-0C41-4649-8D22-537E38CB4570
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappdatabasebackupsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppDatabaseBackupSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppDatabaseBackupSetting.md
ms.openlocfilehash: 29d85284261b5885c90bcd50b1d54a580b53e10d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676285"
---
# <span data-ttu-id="d272d-101">New-AzWebAppDatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="d272d-101">New-AzWebAppDatabaseBackupSetting</span></span>

## <span data-ttu-id="d272d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d272d-102">SYNOPSIS</span></span>

## <span data-ttu-id="d272d-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d272d-103">SYNTAX</span></span>

```
New-AzWebAppDatabaseBackupSetting [-Name] <String> [-DatabaseType] <String> [-ConnectionString] <String>
 [[-ConnectionStringName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d272d-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d272d-104">DESCRIPTION</span></span>
<span data-ttu-id="d272d-105">Il cmdlet **New-AzWebAppDatabaseBackupSetting** crea una nuova impostazione di backup di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="d272d-105">The **New-AzWebAppDatabaseBackupSetting** cmdlet creates a new Azure Web App Backup setting.</span></span>

## <span data-ttu-id="d272d-106">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d272d-106">EXAMPLES</span></span>

### <span data-ttu-id="d272d-107">1:</span><span class="sxs-lookup"><span data-stu-id="d272d-107">1:</span></span>
```
PS C:\> New-AzWebAppDatabaseBackupSetting -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -ConnectionString "MyConnectionString" -DatabaseType "SqlAzure"
```

<span data-ttu-id="d272d-108">Crea un'impostazione di backup del database (stringa di connessione) di tipo sqlazure per l'app specificata ContosoWebApp che si trova all'interno del gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="d272d-108">Creates a database backup setting (connection string) of type SqlAzure for the specified app ContosoWebApp that is within resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="d272d-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d272d-109">PARAMETERS</span></span>

### <span data-ttu-id="d272d-110">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="d272d-110">-ConnectionString</span></span>
<span data-ttu-id="d272d-111">Stringa di connessione</span><span class="sxs-lookup"><span data-stu-id="d272d-111">Connection String</span></span>

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

### <span data-ttu-id="d272d-112">-ConnectionStringname</span><span class="sxs-lookup"><span data-stu-id="d272d-112">-ConnectionStringName</span></span>
<span data-ttu-id="d272d-113">Nome stringa di connessione</span><span class="sxs-lookup"><span data-stu-id="d272d-113">Connection String Name</span></span>

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

### <span data-ttu-id="d272d-114">-DatabaseType</span><span class="sxs-lookup"><span data-stu-id="d272d-114">-DatabaseType</span></span>
<span data-ttu-id="d272d-115">Tipo di database (ad esempio "sqlazure" o "MySql")</span><span class="sxs-lookup"><span data-stu-id="d272d-115">Database Type ( e.g. "SqlAzure" or "MySql" )</span></span>

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

### <span data-ttu-id="d272d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d272d-116">-DefaultProfile</span></span>
<span data-ttu-id="d272d-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d272d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d272d-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="d272d-118">-Name</span></span>
<span data-ttu-id="d272d-119">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="d272d-119">WebApp Name</span></span>

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

### <span data-ttu-id="d272d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d272d-120">CommonParameters</span></span>
<span data-ttu-id="d272d-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d272d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d272d-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d272d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d272d-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d272d-123">INPUTS</span></span>

### <span data-ttu-id="d272d-124">System. String</span><span class="sxs-lookup"><span data-stu-id="d272d-124">System.String</span></span>

## <span data-ttu-id="d272d-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d272d-125">OUTPUTS</span></span>

### <span data-ttu-id="d272d-126">Microsoft. Azure. Management. website. Models. DatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="d272d-126">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting</span></span>

## <span data-ttu-id="d272d-127">Note</span><span class="sxs-lookup"><span data-stu-id="d272d-127">NOTES</span></span>

## <span data-ttu-id="d272d-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d272d-128">RELATED LINKS</span></span>
