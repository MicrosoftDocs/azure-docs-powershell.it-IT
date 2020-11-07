---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackup.md
ms.openlocfilehash: 65748ed269a7cb42914c98549c68be32812f71f3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864566"
---
# <span data-ttu-id="9aed6-101">Get-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="9aed6-101">Get-AzWebAppBackup</span></span>

## <span data-ttu-id="9aed6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9aed6-102">SYNOPSIS</span></span>

## <span data-ttu-id="9aed6-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9aed6-103">SYNTAX</span></span>

### <span data-ttu-id="9aed6-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="9aed6-104">FromResourceName</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9aed6-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="9aed6-105">FromWebApp</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9aed6-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9aed6-106">DESCRIPTION</span></span>
<span data-ttu-id="9aed6-107">Il cmdlet **Get-AzWebAppBackup** ottiene il backup specificato di un'app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="9aed6-107">The **Get-AzWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="9aed6-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9aed6-108">EXAMPLES</span></span>

### <span data-ttu-id="9aed6-109">1:</span><span class="sxs-lookup"><span data-stu-id="9aed6-109">1:</span></span>
```
PS C:\>Get-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="9aed6-110">Questo comando ottiene il backup con ID "12345" dall'app Web denominata WebAppStandard che appartiene al gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="9aed6-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="9aed6-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9aed6-111">PARAMETERS</span></span>

### <span data-ttu-id="9aed6-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="9aed6-112">-BackupId</span></span>
<span data-ttu-id="9aed6-113">ID backup</span><span class="sxs-lookup"><span data-stu-id="9aed6-113">Backup Id</span></span>

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

### <span data-ttu-id="9aed6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9aed6-114">-DefaultProfile</span></span>
<span data-ttu-id="9aed6-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9aed6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9aed6-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="9aed6-116">-Name</span></span>
<span data-ttu-id="9aed6-117">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="9aed6-117">Webapp Name</span></span>

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

### <span data-ttu-id="9aed6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9aed6-118">-ResourceGroupName</span></span>
<span data-ttu-id="9aed6-119">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="9aed6-119">Resource Group Name</span></span>

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

### <span data-ttu-id="9aed6-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="9aed6-120">-Slot</span></span>
<span data-ttu-id="9aed6-121">Nome slot</span><span class="sxs-lookup"><span data-stu-id="9aed6-121">Slot Name</span></span>

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

### <span data-ttu-id="9aed6-122">-Web App</span><span class="sxs-lookup"><span data-stu-id="9aed6-122">-WebApp</span></span>
<span data-ttu-id="9aed6-123">Web App con pipe</span><span class="sxs-lookup"><span data-stu-id="9aed6-123">Piped WebApp</span></span>

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

### <span data-ttu-id="9aed6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9aed6-124">CommonParameters</span></span>
<span data-ttu-id="9aed6-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9aed6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9aed6-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9aed6-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9aed6-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9aed6-127">INPUTS</span></span>

### <span data-ttu-id="9aed6-128">System. String</span><span class="sxs-lookup"><span data-stu-id="9aed6-128">System.String</span></span>

### <span data-ttu-id="9aed6-129">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="9aed6-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="9aed6-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9aed6-130">OUTPUTS</span></span>

### <span data-ttu-id="9aed6-131">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="9aed6-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="9aed6-132">Note</span><span class="sxs-lookup"><span data-stu-id="9aed6-132">NOTES</span></span>

## <span data-ttu-id="9aed6-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9aed6-133">RELATED LINKS</span></span>
