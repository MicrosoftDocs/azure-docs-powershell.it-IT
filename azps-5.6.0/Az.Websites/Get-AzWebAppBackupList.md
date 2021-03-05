---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappbackuplist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
ms.openlocfilehash: f70caa984fde48db6b2d1d147ebf62f544f2ed9f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972381"
---
# <span data-ttu-id="45077-101">Get-AzWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="45077-101">Get-AzWebAppBackupList</span></span>

## <span data-ttu-id="45077-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45077-102">SYNOPSIS</span></span>

## <span data-ttu-id="45077-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="45077-103">SYNTAX</span></span>

### <span data-ttu-id="45077-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="45077-104">FromResourceName</span></span>
```
Get-AzWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45077-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="45077-105">FromWebApp</span></span>
```
Get-AzWebAppBackupList [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45077-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="45077-106">DESCRIPTION</span></span>
<span data-ttu-id="45077-107">Il **cmdlet Get-AzWebAppBackupList** ottiene un elenco di backup per un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="45077-107">The **Get-AzWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="45077-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="45077-108">EXAMPLES</span></span>

### <span data-ttu-id="45077-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="45077-109">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="45077-110">Questo comando restituisce un elenco di backup relativo alla WebApp WebAppStandard associata al gruppo di risorse ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="45077-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="45077-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45077-111">PARAMETERS</span></span>

### <span data-ttu-id="45077-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45077-112">-DefaultProfile</span></span>
<span data-ttu-id="45077-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="45077-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45077-114">-Name</span><span class="sxs-lookup"><span data-stu-id="45077-114">-Name</span></span>
<span data-ttu-id="45077-115">Nome WebApp</span><span class="sxs-lookup"><span data-stu-id="45077-115">WebApp Name</span></span>

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

### <span data-ttu-id="45077-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45077-116">-ResourceGroupName</span></span>
<span data-ttu-id="45077-117">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="45077-117">Resource Group Name</span></span>

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

### <span data-ttu-id="45077-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="45077-118">-Slot</span></span>
<span data-ttu-id="45077-119">Nome slot</span><span class="sxs-lookup"><span data-stu-id="45077-119">Slot name</span></span>

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

### <span data-ttu-id="45077-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="45077-120">-WebApp</span></span>
<span data-ttu-id="45077-121">Piped WebApp</span><span class="sxs-lookup"><span data-stu-id="45077-121">Piped WebApp</span></span>

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

### <span data-ttu-id="45077-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45077-122">CommonParameters</span></span>
<span data-ttu-id="45077-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45077-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45077-124">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45077-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45077-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="45077-125">INPUTS</span></span>

### <span data-ttu-id="45077-126">System.String</span><span class="sxs-lookup"><span data-stu-id="45077-126">System.String</span></span>

### <span data-ttu-id="45077-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="45077-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="45077-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="45077-128">OUTPUTS</span></span>

### <span data-ttu-id="45077-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="45077-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="45077-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="45077-130">NOTES</span></span>

## <span data-ttu-id="45077-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="45077-131">RELATED LINKS</span></span>
