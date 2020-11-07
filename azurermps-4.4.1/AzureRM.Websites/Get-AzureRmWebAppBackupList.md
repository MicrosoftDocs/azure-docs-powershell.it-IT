---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupList.md
ms.openlocfilehash: 02c83e79b5f56d4ef9a6d7730efb5cf5c42a9da8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686533"
---
# <span data-ttu-id="ba4e4-101">Get-AzureRmWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="ba4e4-101">Get-AzureRmWebAppBackupList</span></span>

## <span data-ttu-id="ba4e4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ba4e4-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba4e4-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ba4e4-103">SYNTAX</span></span>

### <span data-ttu-id="ba4e4-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="ba4e4-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba4e4-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="ba4e4-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupList [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba4e4-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ba4e4-106">DESCRIPTION</span></span>
<span data-ttu-id="ba4e4-107">Il cmdlet **Get-AzureRmWebAppBackupList** ottiene un elenco di backup per un'app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="ba4e4-107">The **Get-AzureRmWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="ba4e4-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ba4e4-108">EXAMPLES</span></span>

### <span data-ttu-id="ba4e4-109">1:</span><span class="sxs-lookup"><span data-stu-id="ba4e4-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="ba4e4-110">Questo comando restituisce un elenco di backup relativo a Web App WebAppStandard associato al gruppo di risorse ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ba4e4-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="ba4e4-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ba4e4-111">PARAMETERS</span></span>

### <span data-ttu-id="ba4e4-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="ba4e4-112">-Name</span></span>
<span data-ttu-id="ba4e4-113">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="ba4e4-113">WebApp Name</span></span>

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

### <span data-ttu-id="ba4e4-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba4e4-114">-ResourceGroupName</span></span>
<span data-ttu-id="ba4e4-115">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="ba4e4-115">Resource Group Name</span></span>

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

### <span data-ttu-id="ba4e4-116">-Slot</span><span class="sxs-lookup"><span data-stu-id="ba4e4-116">-Slot</span></span>
<span data-ttu-id="ba4e4-117">Nome slot</span><span class="sxs-lookup"><span data-stu-id="ba4e4-117">Slot name</span></span>

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

### <span data-ttu-id="ba4e4-118">-Web App</span><span class="sxs-lookup"><span data-stu-id="ba4e4-118">-WebApp</span></span>
<span data-ttu-id="ba4e4-119">Web App con pipe</span><span class="sxs-lookup"><span data-stu-id="ba4e4-119">Piped WebApp</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba4e4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba4e4-120">-DefaultProfile</span></span>
<span data-ttu-id="ba4e4-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ba4e4-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba4e4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba4e4-122">CommonParameters</span></span>
<span data-ttu-id="ba4e4-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba4e4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba4e4-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba4e4-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba4e4-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ba4e4-125">INPUTS</span></span>

### <span data-ttu-id="ba4e4-126">Sito</span><span class="sxs-lookup"><span data-stu-id="ba4e4-126">Site</span></span>
<span data-ttu-id="ba4e4-127">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="ba4e4-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="ba4e4-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ba4e4-128">OUTPUTS</span></span>

### <span data-ttu-id="ba4e4-129">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. AzureWebAppBackup []</span><span class="sxs-lookup"><span data-stu-id="ba4e4-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup[]</span></span>

## <span data-ttu-id="ba4e4-130">Note</span><span class="sxs-lookup"><span data-stu-id="ba4e4-130">NOTES</span></span>

## <span data-ttu-id="ba4e4-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ba4e4-131">RELATED LINKS</span></span>

