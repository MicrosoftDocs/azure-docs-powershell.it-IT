---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappbackuplist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppBackupList.md
ms.openlocfilehash: 057bebde5eada143c9ee00260a1406fdceae9436
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861945"
---
# <span data-ttu-id="27c26-101">Get-AzWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="27c26-101">Get-AzWebAppBackupList</span></span>

## <span data-ttu-id="27c26-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="27c26-102">SYNOPSIS</span></span>

## <span data-ttu-id="27c26-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="27c26-103">SYNTAX</span></span>

### <span data-ttu-id="27c26-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="27c26-104">FromResourceName</span></span>
```
Get-AzWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27c26-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="27c26-105">FromWebApp</span></span>
```
Get-AzWebAppBackupList [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27c26-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="27c26-106">DESCRIPTION</span></span>
<span data-ttu-id="27c26-107">Il cmdlet **Get-AzWebAppBackupList** ottiene un elenco di backup per un'app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="27c26-107">The **Get-AzWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="27c26-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="27c26-108">EXAMPLES</span></span>

### <span data-ttu-id="27c26-109">1:</span><span class="sxs-lookup"><span data-stu-id="27c26-109">1:</span></span>
```
PS C:\>Get-AzWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="27c26-110">Questo comando restituisce un elenco di backup relativo a Web App WebAppStandard associato al gruppo di risorse ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="27c26-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="27c26-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="27c26-111">PARAMETERS</span></span>

### <span data-ttu-id="27c26-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27c26-112">-DefaultProfile</span></span>
<span data-ttu-id="27c26-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="27c26-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27c26-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="27c26-114">-Name</span></span>
<span data-ttu-id="27c26-115">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="27c26-115">WebApp Name</span></span>

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

### <span data-ttu-id="27c26-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27c26-116">-ResourceGroupName</span></span>
<span data-ttu-id="27c26-117">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="27c26-117">Resource Group Name</span></span>

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

### <span data-ttu-id="27c26-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="27c26-118">-Slot</span></span>
<span data-ttu-id="27c26-119">Nome slot</span><span class="sxs-lookup"><span data-stu-id="27c26-119">Slot name</span></span>

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

### <span data-ttu-id="27c26-120">-Web App</span><span class="sxs-lookup"><span data-stu-id="27c26-120">-WebApp</span></span>
<span data-ttu-id="27c26-121">Web App con pipe</span><span class="sxs-lookup"><span data-stu-id="27c26-121">Piped WebApp</span></span>

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

### <span data-ttu-id="27c26-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27c26-122">CommonParameters</span></span>
<span data-ttu-id="27c26-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27c26-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27c26-124">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27c26-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27c26-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="27c26-125">INPUTS</span></span>

### <span data-ttu-id="27c26-126">Sito</span><span class="sxs-lookup"><span data-stu-id="27c26-126">Site</span></span>
<span data-ttu-id="27c26-127">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="27c26-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="27c26-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="27c26-128">OUTPUTS</span></span>

### <span data-ttu-id="27c26-129">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. AzureWebAppBackup []</span><span class="sxs-lookup"><span data-stu-id="27c26-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup[]</span></span>

## <span data-ttu-id="27c26-130">Note</span><span class="sxs-lookup"><span data-stu-id="27c26-130">NOTES</span></span>

## <span data-ttu-id="27c26-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="27c26-131">RELATED LINKS</span></span>

