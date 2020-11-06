---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackuplist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupList.md
ms.openlocfilehash: f4005df31746b63b2a45fa2c78f254e2d5f24c59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508927"
---
# <span data-ttu-id="7e1b3-101">Get-AzureRmWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="7e1b3-101">Get-AzureRmWebAppBackupList</span></span>

## <span data-ttu-id="7e1b3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7e1b3-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e1b3-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7e1b3-103">SYNTAX</span></span>

### <span data-ttu-id="7e1b3-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="7e1b3-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e1b3-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="7e1b3-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupList [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e1b3-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e1b3-106">DESCRIPTION</span></span>
<span data-ttu-id="7e1b3-107">Il cmdlet **Get-AzureRmWebAppBackupList** ottiene un elenco di backup per un'app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="7e1b3-107">The **Get-AzureRmWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="7e1b3-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7e1b3-108">EXAMPLES</span></span>

### <span data-ttu-id="7e1b3-109">1:</span><span class="sxs-lookup"><span data-stu-id="7e1b3-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="7e1b3-110">Questo comando restituisce un elenco di backup relativo a Web App WebAppStandard associato al gruppo di risorse ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7e1b3-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="7e1b3-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7e1b3-111">PARAMETERS</span></span>

### <span data-ttu-id="7e1b3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e1b3-112">-DefaultProfile</span></span>
<span data-ttu-id="7e1b3-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7e1b3-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e1b3-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="7e1b3-114">-Name</span></span>
<span data-ttu-id="7e1b3-115">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="7e1b3-115">WebApp Name</span></span>

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

### <span data-ttu-id="7e1b3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e1b3-116">-ResourceGroupName</span></span>
<span data-ttu-id="7e1b3-117">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="7e1b3-117">Resource Group Name</span></span>

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

### <span data-ttu-id="7e1b3-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="7e1b3-118">-Slot</span></span>
<span data-ttu-id="7e1b3-119">Nome slot</span><span class="sxs-lookup"><span data-stu-id="7e1b3-119">Slot name</span></span>

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

### <span data-ttu-id="7e1b3-120">-Web App</span><span class="sxs-lookup"><span data-stu-id="7e1b3-120">-WebApp</span></span>
<span data-ttu-id="7e1b3-121">Web App con pipe</span><span class="sxs-lookup"><span data-stu-id="7e1b3-121">Piped WebApp</span></span>

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

### <span data-ttu-id="7e1b3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e1b3-122">CommonParameters</span></span>
<span data-ttu-id="7e1b3-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e1b3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e1b3-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e1b3-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e1b3-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7e1b3-125">INPUTS</span></span>

### <span data-ttu-id="7e1b3-126">System. String</span><span class="sxs-lookup"><span data-stu-id="7e1b3-126">System.String</span></span>

### <span data-ttu-id="7e1b3-127">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="7e1b3-127">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="7e1b3-128">Parametri: Web App (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7e1b3-128">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="7e1b3-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7e1b3-129">OUTPUTS</span></span>

### <span data-ttu-id="7e1b3-130">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="7e1b3-130">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="7e1b3-131">Note</span><span class="sxs-lookup"><span data-stu-id="7e1b3-131">NOTES</span></span>

## <span data-ttu-id="7e1b3-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7e1b3-132">RELATED LINKS</span></span>
