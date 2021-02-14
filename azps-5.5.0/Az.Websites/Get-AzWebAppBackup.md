---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackup.md
ms.openlocfilehash: e8c3f7543062613527e7f52be2cd6493f53c5f60
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188718"
---
# <span data-ttu-id="b5b5a-101">Get-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="b5b5a-101">Get-AzWebAppBackup</span></span>

## <span data-ttu-id="b5b5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5b5a-102">SYNOPSIS</span></span>

## <span data-ttu-id="b5b5a-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b5b5a-103">SYNTAX</span></span>

### <span data-ttu-id="b5b5a-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="b5b5a-104">FromResourceName</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5b5a-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="b5b5a-105">FromWebApp</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b5b5a-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b5b5a-106">DESCRIPTION</span></span>
<span data-ttu-id="b5b5a-107">Il cmdlet **Get-AzWebAppBackup** ottiene il backup specificato di un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="b5b5a-107">The **Get-AzWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="b5b5a-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b5b5a-108">EXAMPLES</span></span>

### <span data-ttu-id="b5b5a-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b5b5a-109">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="b5b5a-110">Questo comando recupera il backup con ID "12345" dall'app Web denominata WebAppStandard che appartiene al gruppo di risorse Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="b5b5a-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="b5b5a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5b5a-111">PARAMETERS</span></span>

### <span data-ttu-id="b5b5a-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="b5b5a-112">-BackupId</span></span>
<span data-ttu-id="b5b5a-113">Backup Id</span><span class="sxs-lookup"><span data-stu-id="b5b5a-113">Backup Id</span></span>

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

### <span data-ttu-id="b5b5a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5b5a-114">-DefaultProfile</span></span>
<span data-ttu-id="b5b5a-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b5b5a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5b5a-116">-Name</span><span class="sxs-lookup"><span data-stu-id="b5b5a-116">-Name</span></span>
<span data-ttu-id="b5b5a-117">Nome app Web</span><span class="sxs-lookup"><span data-stu-id="b5b5a-117">Webapp Name</span></span>

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

### <span data-ttu-id="b5b5a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5b5a-118">-ResourceGroupName</span></span>
<span data-ttu-id="b5b5a-119">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="b5b5a-119">Resource Group Name</span></span>

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

### <span data-ttu-id="b5b5a-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="b5b5a-120">-Slot</span></span>
<span data-ttu-id="b5b5a-121">Nome slot</span><span class="sxs-lookup"><span data-stu-id="b5b5a-121">Slot Name</span></span>

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

### <span data-ttu-id="b5b5a-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="b5b5a-122">-WebApp</span></span>
<span data-ttu-id="b5b5a-123">Piped WebApp</span><span class="sxs-lookup"><span data-stu-id="b5b5a-123">Piped WebApp</span></span>

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

### <span data-ttu-id="b5b5a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5b5a-124">CommonParameters</span></span>
<span data-ttu-id="b5b5a-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5b5a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5b5a-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5b5a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5b5a-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="b5b5a-127">INPUTS</span></span>

### <span data-ttu-id="b5b5a-128">System.String</span><span class="sxs-lookup"><span data-stu-id="b5b5a-128">System.String</span></span>

### <span data-ttu-id="b5b5a-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="b5b5a-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="b5b5a-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b5b5a-130">OUTPUTS</span></span>

### <span data-ttu-id="b5b5a-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="b5b5a-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="b5b5a-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="b5b5a-132">NOTES</span></span>

## <span data-ttu-id="b5b5a-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b5b5a-133">RELATED LINKS</span></span>
