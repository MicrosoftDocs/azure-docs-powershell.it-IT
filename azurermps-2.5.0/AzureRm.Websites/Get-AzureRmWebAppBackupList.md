---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackuplist
schema: 2.0.0
ms.openlocfilehash: ef409c62d56a95d36f1e7c9a02018b281c00e3c9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865992"
---
# <span data-ttu-id="e8ffe-101">Get-AzureRmWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="e8ffe-101">Get-AzureRmWebAppBackupList</span></span>

## <span data-ttu-id="e8ffe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e8ffe-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8ffe-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e8ffe-103">SYNTAX</span></span>

### <span data-ttu-id="e8ffe-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="e8ffe-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8ffe-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="e8ffe-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupList [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8ffe-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e8ffe-106">DESCRIPTION</span></span>
<span data-ttu-id="e8ffe-107">Il cmdlet **Get-AzureRmWebAppBackupList** ottiene un elenco di backup per un'app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="e8ffe-107">The **Get-AzureRmWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="e8ffe-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e8ffe-108">EXAMPLES</span></span>

### <span data-ttu-id="e8ffe-109">1:</span><span class="sxs-lookup"><span data-stu-id="e8ffe-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="e8ffe-110">Questo comando restituisce un elenco di backup relativo a Web App WebAppStandard associato al gruppo di risorse ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e8ffe-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="e8ffe-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e8ffe-111">PARAMETERS</span></span>

### <span data-ttu-id="e8ffe-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8ffe-112">-DefaultProfile</span></span>
<span data-ttu-id="e8ffe-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e8ffe-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8ffe-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="e8ffe-114">-Name</span></span>
<span data-ttu-id="e8ffe-115">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="e8ffe-115">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8ffe-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8ffe-116">-ResourceGroupName</span></span>
<span data-ttu-id="e8ffe-117">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="e8ffe-117">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8ffe-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="e8ffe-118">-Slot</span></span>
<span data-ttu-id="e8ffe-119">Nome slot</span><span class="sxs-lookup"><span data-stu-id="e8ffe-119">Slot name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8ffe-120">-Web App</span><span class="sxs-lookup"><span data-stu-id="e8ffe-120">-WebApp</span></span>
<span data-ttu-id="e8ffe-121">Web App con pipe</span><span class="sxs-lookup"><span data-stu-id="e8ffe-121">Piped WebApp</span></span>

```yaml
Type: Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8ffe-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8ffe-122">CommonParameters</span></span>
<span data-ttu-id="e8ffe-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8ffe-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8ffe-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8ffe-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8ffe-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e8ffe-125">INPUTS</span></span>

### <span data-ttu-id="e8ffe-126">Sito</span><span class="sxs-lookup"><span data-stu-id="e8ffe-126">Site</span></span>
<span data-ttu-id="e8ffe-127">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="e8ffe-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="e8ffe-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e8ffe-128">OUTPUTS</span></span>

### <span data-ttu-id="e8ffe-129">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. AzureWebAppBackup []</span><span class="sxs-lookup"><span data-stu-id="e8ffe-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup[]</span></span>

## <span data-ttu-id="e8ffe-130">Note</span><span class="sxs-lookup"><span data-stu-id="e8ffe-130">NOTES</span></span>

## <span data-ttu-id="e8ffe-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e8ffe-131">RELATED LINKS</span></span>

