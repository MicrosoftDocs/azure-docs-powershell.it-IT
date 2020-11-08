---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 65A78654-A490-4B60-8C16-B0CC597EE995
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppBackup.md
ms.openlocfilehash: 04184483d2bda7495014d3efd8ecf35b4d3b6864
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018682"
---
# <span data-ttu-id="3a159-101">Remove-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="3a159-101">Remove-AzWebAppBackup</span></span>

## <span data-ttu-id="3a159-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3a159-102">SYNOPSIS</span></span>

## <span data-ttu-id="3a159-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3a159-103">SYNTAX</span></span>

### <span data-ttu-id="3a159-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="3a159-104">FromResourceName</span></span>
```
Remove-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a159-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="3a159-105">FromWebApp</span></span>
```
Remove-AzWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3a159-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a159-106">DESCRIPTION</span></span>
<span data-ttu-id="3a159-107">Il cmdlet **Remove-AzWebAppBackup** rimuove il backup specificato di una Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="3a159-107">The **Remove-AzWebAppBackup** cmdlet removes the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="3a159-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3a159-108">EXAMPLES</span></span>

### <span data-ttu-id="3a159-109">1:</span><span class="sxs-lookup"><span data-stu-id="3a159-109">1:</span></span>
```
PS C:\>Remove-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="3a159-110">Questo comando rimuove il backup con il backup con ID "12345" dall'app Web denominata WebAppStandard che appartiene al gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="3a159-110">This command removes the backup with backup with ID of "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="3a159-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3a159-111">PARAMETERS</span></span>

### <span data-ttu-id="3a159-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="3a159-112">-BackupId</span></span>
<span data-ttu-id="3a159-113">ID backup</span><span class="sxs-lookup"><span data-stu-id="3a159-113">Backup Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a159-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a159-114">-DefaultProfile</span></span>
<span data-ttu-id="3a159-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3a159-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a159-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="3a159-116">-Name</span></span>
<span data-ttu-id="3a159-117">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="3a159-117">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a159-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a159-118">-ResourceGroupName</span></span>
<span data-ttu-id="3a159-119">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="3a159-119">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a159-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="3a159-120">-Slot</span></span>
<span data-ttu-id="3a159-121">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="3a159-121">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a159-122">-Web App</span><span class="sxs-lookup"><span data-stu-id="3a159-122">-WebApp</span></span>
<span data-ttu-id="3a159-123">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="3a159-123">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a159-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a159-124">CommonParameters</span></span>
<span data-ttu-id="3a159-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a159-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a159-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a159-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a159-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3a159-127">INPUTS</span></span>

### <span data-ttu-id="3a159-128">System. String</span><span class="sxs-lookup"><span data-stu-id="3a159-128">System.String</span></span>

### <span data-ttu-id="3a159-129">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="3a159-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="3a159-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3a159-130">OUTPUTS</span></span>

### <span data-ttu-id="3a159-131">Microsoft. Azure. Management. website. Models. BackupItem</span><span class="sxs-lookup"><span data-stu-id="3a159-131">Microsoft.Azure.Management.WebSites.Models.BackupItem</span></span>

## <span data-ttu-id="3a159-132">Note</span><span class="sxs-lookup"><span data-stu-id="3a159-132">NOTES</span></span>

## <span data-ttu-id="3a159-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3a159-133">RELATED LINKS</span></span>
