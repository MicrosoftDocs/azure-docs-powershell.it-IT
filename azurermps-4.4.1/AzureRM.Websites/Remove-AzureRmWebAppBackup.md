---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 65A78654-A490-4B60-8C16-B0CC597EE995
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppBackup.md
ms.openlocfilehash: ba7255c41b5851b1f34b2ff7a1523c691925bae0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521493"
---
# <span data-ttu-id="a30a4-101">Remove-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="a30a4-101">Remove-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="a30a4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a30a4-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a30a4-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a30a4-103">SYNTAX</span></span>

### <span data-ttu-id="a30a4-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="a30a4-104">FromResourceName</span></span>
```
Remove-AzureRmWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a30a4-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="a30a4-105">FromWebApp</span></span>
```
Remove-AzureRmWebAppBackup [-BackupId] <String> [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a30a4-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a30a4-106">DESCRIPTION</span></span>
<span data-ttu-id="a30a4-107">Il cmdlet **Remove-AzureRmWebAppBackup** rimuove il backup specificato di una Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="a30a4-107">The **Remove-AzureRmWebAppBackup** cmdlet removes the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="a30a4-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a30a4-108">EXAMPLES</span></span>

### <span data-ttu-id="a30a4-109">1:</span><span class="sxs-lookup"><span data-stu-id="a30a4-109">1:</span></span>
```
PS C:\>Remove-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="a30a4-110">Questo comando rimuove il backup con il backup con ID "12345" dall'app Web denominata WebAppStandard che appartiene al gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="a30a4-110">This command removes the backup with backup with ID of "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="a30a4-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a30a4-111">PARAMETERS</span></span>

### <span data-ttu-id="a30a4-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="a30a4-112">-BackupId</span></span>
<span data-ttu-id="a30a4-113">ID backup</span><span class="sxs-lookup"><span data-stu-id="a30a4-113">Backup Id</span></span>

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

### <span data-ttu-id="a30a4-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="a30a4-114">-Name</span></span>
<span data-ttu-id="a30a4-115">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="a30a4-115">WebApp Name</span></span>

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

### <span data-ttu-id="a30a4-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a30a4-116">-ResourceGroupName</span></span>
<span data-ttu-id="a30a4-117">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="a30a4-117">Resource Group Name</span></span>

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

### <span data-ttu-id="a30a4-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="a30a4-118">-Slot</span></span>
<span data-ttu-id="a30a4-119">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="a30a4-119">WebApp Slot Name</span></span>

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

### <span data-ttu-id="a30a4-120">-Web App</span><span class="sxs-lookup"><span data-stu-id="a30a4-120">-WebApp</span></span>
<span data-ttu-id="a30a4-121">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="a30a4-121">WebApp Object</span></span>

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

### <span data-ttu-id="a30a4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a30a4-122">-DefaultProfile</span></span>
<span data-ttu-id="a30a4-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a30a4-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a30a4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a30a4-124">CommonParameters</span></span>
<span data-ttu-id="a30a4-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a30a4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a30a4-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a30a4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a30a4-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a30a4-127">INPUTS</span></span>

### <span data-ttu-id="a30a4-128">Sito</span><span class="sxs-lookup"><span data-stu-id="a30a4-128">Site</span></span>
<span data-ttu-id="a30a4-129">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="a30a4-129">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="a30a4-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a30a4-130">OUTPUTS</span></span>

### <span data-ttu-id="a30a4-131">Microsoft. Azure. Management. website. Models. BackupItem</span><span class="sxs-lookup"><span data-stu-id="a30a4-131">Microsoft.Azure.Management.WebSites.Models.BackupItem</span></span>

## <span data-ttu-id="a30a4-132">Note</span><span class="sxs-lookup"><span data-stu-id="a30a4-132">NOTES</span></span>

## <span data-ttu-id="a30a4-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a30a4-133">RELATED LINKS</span></span>

