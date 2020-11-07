---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 22ACB910-0C41-4649-8D22-537E38CB4570
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappdatabasebackupsetting
schema: 2.0.0
ms.openlocfilehash: f44b6f370b1431a5baf1a0686b4e893653327227
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866947"
---
# <span data-ttu-id="80b27-101">New-AzureRmWebAppDatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="80b27-101">New-AzureRmWebAppDatabaseBackupSetting</span></span>

## <span data-ttu-id="80b27-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="80b27-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80b27-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="80b27-103">SYNTAX</span></span>

```
New-AzureRmWebAppDatabaseBackupSetting [-Name] <String> [-DatabaseType] <String> [-ConnectionString] <String>
 [[-ConnectionStringName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80b27-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="80b27-104">DESCRIPTION</span></span>
<span data-ttu-id="80b27-105">Il cmdlet **New-AzureRmWebAppDatabaseBackupSetting** crea una nuova impostazione di backup di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="80b27-105">The **New-AzureRmWebAppDatabaseBackupSetting** cmdlet creates a new Azure Web App Backup setting.</span></span>

## <span data-ttu-id="80b27-106">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="80b27-106">EXAMPLES</span></span>

### <span data-ttu-id="80b27-107">1:</span><span class="sxs-lookup"><span data-stu-id="80b27-107">1:</span></span>
```
PS C:\> New-AzureRmWebAppDatabaseBackupSetting -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -ConnectionString "MyConnectionString" -DatabaseType "SqlAzure"
```

<span data-ttu-id="80b27-108">Crea un'impostazione di backup del database (stringa di connessione) di tipo sqlazure per l'app specificata ContosoWebApp che si trova all'interno del gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="80b27-108">Creates a database backup setting (connection string) of type SqlAzure for the specified app ContosoWebApp that is within resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="80b27-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="80b27-109">PARAMETERS</span></span>

### <span data-ttu-id="80b27-110">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="80b27-110">-ConnectionString</span></span>
<span data-ttu-id="80b27-111">Stringa di connessione</span><span class="sxs-lookup"><span data-stu-id="80b27-111">Connection String</span></span>

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

### <span data-ttu-id="80b27-112">-ConnectionStringname</span><span class="sxs-lookup"><span data-stu-id="80b27-112">-ConnectionStringName</span></span>
<span data-ttu-id="80b27-113">Nome stringa di connessione</span><span class="sxs-lookup"><span data-stu-id="80b27-113">Connection String Name</span></span>

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

### <span data-ttu-id="80b27-114">-DatabaseType</span><span class="sxs-lookup"><span data-stu-id="80b27-114">-DatabaseType</span></span>
<span data-ttu-id="80b27-115">Tipo di database (ad esempio "sqlazure" o "MySql")</span><span class="sxs-lookup"><span data-stu-id="80b27-115">Database Type ( e.g. "SqlAzure" or "MySql" )</span></span>

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

### <span data-ttu-id="80b27-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80b27-116">-DefaultProfile</span></span>
<span data-ttu-id="80b27-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="80b27-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80b27-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="80b27-118">-Name</span></span>
<span data-ttu-id="80b27-119">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="80b27-119">WebApp Name</span></span>

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

### <span data-ttu-id="80b27-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80b27-120">CommonParameters</span></span>
<span data-ttu-id="80b27-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80b27-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80b27-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80b27-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80b27-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="80b27-123">INPUTS</span></span>

### <span data-ttu-id="80b27-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="80b27-124">None</span></span>
<span data-ttu-id="80b27-125">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="80b27-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="80b27-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="80b27-126">OUTPUTS</span></span>

### <span data-ttu-id="80b27-127">Microsoft. Azure. Management. website. Models. DatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="80b27-127">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting</span></span>

## <span data-ttu-id="80b27-128">Note</span><span class="sxs-lookup"><span data-stu-id="80b27-128">NOTES</span></span>

## <span data-ttu-id="80b27-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="80b27-129">RELATED LINKS</span></span>

