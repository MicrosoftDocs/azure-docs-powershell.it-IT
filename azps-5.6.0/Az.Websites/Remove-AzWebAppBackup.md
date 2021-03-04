---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 65A78654-A490-4B60-8C16-B0CC597EE995
online version: https://docs.microsoft.com/powershell/module/az.websites/remove-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppBackup.md
ms.openlocfilehash: d6bba1b517f238247291af251d9f510d18029af6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994655"
---
# <span data-ttu-id="20d66-101">Remove-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="20d66-101">Remove-AzWebAppBackup</span></span>

## <span data-ttu-id="20d66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20d66-102">SYNOPSIS</span></span>

## <span data-ttu-id="20d66-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="20d66-103">SYNTAX</span></span>

### <span data-ttu-id="20d66-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="20d66-104">FromResourceName</span></span>
```
Remove-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20d66-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="20d66-105">FromWebApp</span></span>
```
Remove-AzWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="20d66-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="20d66-106">DESCRIPTION</span></span>
<span data-ttu-id="20d66-107">Il cmdlet **Remove-AzWebAppBackup** rimuove il backup specificato di un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="20d66-107">The **Remove-AzWebAppBackup** cmdlet removes the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="20d66-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="20d66-108">EXAMPLES</span></span>

### <span data-ttu-id="20d66-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="20d66-109">Example 1</span></span>
```powershell
PS C:\>Remove-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="20d66-110">Questo comando rimuove il backup con backup con ID "12345" dall'app Web denominata WebAppStandard che appartiene al gruppo di risorse Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="20d66-110">This command removes the backup with backup with ID of "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="20d66-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="20d66-111">PARAMETERS</span></span>

### <span data-ttu-id="20d66-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="20d66-112">-BackupId</span></span>
<span data-ttu-id="20d66-113">Backup Id</span><span class="sxs-lookup"><span data-stu-id="20d66-113">Backup Id</span></span>

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

### <span data-ttu-id="20d66-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20d66-114">-DefaultProfile</span></span>
<span data-ttu-id="20d66-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="20d66-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20d66-116">-Name</span><span class="sxs-lookup"><span data-stu-id="20d66-116">-Name</span></span>
<span data-ttu-id="20d66-117">Nome WebApp</span><span class="sxs-lookup"><span data-stu-id="20d66-117">WebApp Name</span></span>

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

### <span data-ttu-id="20d66-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20d66-118">-ResourceGroupName</span></span>
<span data-ttu-id="20d66-119">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="20d66-119">Resource Group Name</span></span>

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

### <span data-ttu-id="20d66-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="20d66-120">-Slot</span></span>
<span data-ttu-id="20d66-121">Nome slot WebApp</span><span class="sxs-lookup"><span data-stu-id="20d66-121">WebApp Slot Name</span></span>

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

### <span data-ttu-id="20d66-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="20d66-122">-WebApp</span></span>
<span data-ttu-id="20d66-123">Oggetto WebApp</span><span class="sxs-lookup"><span data-stu-id="20d66-123">WebApp Object</span></span>

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

### <span data-ttu-id="20d66-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20d66-124">CommonParameters</span></span>
<span data-ttu-id="20d66-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20d66-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20d66-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20d66-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20d66-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="20d66-127">INPUTS</span></span>

### <span data-ttu-id="20d66-128">System.String</span><span class="sxs-lookup"><span data-stu-id="20d66-128">System.String</span></span>

### <span data-ttu-id="20d66-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="20d66-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="20d66-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="20d66-130">OUTPUTS</span></span>

### <span data-ttu-id="20d66-131">Microsoft.Azure.Management.WebSites.Models.BackupItem</span><span class="sxs-lookup"><span data-stu-id="20d66-131">Microsoft.Azure.Management.WebSites.Models.BackupItem</span></span>

## <span data-ttu-id="20d66-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="20d66-132">NOTES</span></span>

## <span data-ttu-id="20d66-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="20d66-133">RELATED LINKS</span></span>
