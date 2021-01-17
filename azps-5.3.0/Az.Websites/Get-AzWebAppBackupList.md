---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackuplist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
ms.openlocfilehash: 6ea805f1e3a3711c2efe6faefd73edf06c4b51fd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380754"
---
# <span data-ttu-id="dbcc6-101">Get-AzWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="dbcc6-101">Get-AzWebAppBackupList</span></span>

## <span data-ttu-id="dbcc6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dbcc6-102">SYNOPSIS</span></span>

## <span data-ttu-id="dbcc6-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dbcc6-103">SYNTAX</span></span>

### <span data-ttu-id="dbcc6-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="dbcc6-104">FromResourceName</span></span>
```
Get-AzWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbcc6-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="dbcc6-105">FromWebApp</span></span>
```
Get-AzWebAppBackupList [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbcc6-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dbcc6-106">DESCRIPTION</span></span>
<span data-ttu-id="dbcc6-107">Il cmdlet **Get-AzWebAppBackupList** ottiene un elenco di backup per un'app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="dbcc6-107">The **Get-AzWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="dbcc6-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dbcc6-108">EXAMPLES</span></span>

### <span data-ttu-id="dbcc6-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="dbcc6-109">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="dbcc6-110">Questo comando restituisce un elenco di backup relativo a Web App WebAppStandard associato al gruppo di risorse ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="dbcc6-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="dbcc6-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dbcc6-111">PARAMETERS</span></span>

### <span data-ttu-id="dbcc6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbcc6-112">-DefaultProfile</span></span>
<span data-ttu-id="dbcc6-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dbcc6-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbcc6-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="dbcc6-114">-Name</span></span>
<span data-ttu-id="dbcc6-115">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="dbcc6-115">WebApp Name</span></span>

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

### <span data-ttu-id="dbcc6-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbcc6-116">-ResourceGroupName</span></span>
<span data-ttu-id="dbcc6-117">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="dbcc6-117">Resource Group Name</span></span>

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

### <span data-ttu-id="dbcc6-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="dbcc6-118">-Slot</span></span>
<span data-ttu-id="dbcc6-119">Nome slot</span><span class="sxs-lookup"><span data-stu-id="dbcc6-119">Slot name</span></span>

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

### <span data-ttu-id="dbcc6-120">-Web App</span><span class="sxs-lookup"><span data-stu-id="dbcc6-120">-WebApp</span></span>
<span data-ttu-id="dbcc6-121">Web App con pipe</span><span class="sxs-lookup"><span data-stu-id="dbcc6-121">Piped WebApp</span></span>

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

### <span data-ttu-id="dbcc6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbcc6-122">CommonParameters</span></span>
<span data-ttu-id="dbcc6-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbcc6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbcc6-124">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbcc6-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbcc6-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dbcc6-125">INPUTS</span></span>

### <span data-ttu-id="dbcc6-126">System. String</span><span class="sxs-lookup"><span data-stu-id="dbcc6-126">System.String</span></span>

### <span data-ttu-id="dbcc6-127">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="dbcc6-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="dbcc6-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dbcc6-128">OUTPUTS</span></span>

### <span data-ttu-id="dbcc6-129">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="dbcc6-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="dbcc6-130">Note</span><span class="sxs-lookup"><span data-stu-id="dbcc6-130">NOTES</span></span>

## <span data-ttu-id="dbcc6-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dbcc6-131">RELATED LINKS</span></span>
