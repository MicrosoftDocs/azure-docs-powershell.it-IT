---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 65A78654-A490-4B60-8C16-B0CC597EE995
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebappbackup
schema: 2.0.0
ms.openlocfilehash: ad27e4f9f7e042fa5a649fb06131167f38f1a1be
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866790"
---
# <span data-ttu-id="11803-101">Remove-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="11803-101">Remove-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="11803-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="11803-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11803-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="11803-103">SYNTAX</span></span>

### <span data-ttu-id="11803-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="11803-104">FromResourceName</span></span>
```
Remove-AzureRmWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11803-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="11803-105">FromWebApp</span></span>
```
Remove-AzureRmWebAppBackup [-BackupId] <String> [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="11803-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="11803-106">DESCRIPTION</span></span>
<span data-ttu-id="11803-107">Il cmdlet **Remove-AzureRmWebAppBackup** rimuove il backup specificato di una Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="11803-107">The **Remove-AzureRmWebAppBackup** cmdlet removes the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="11803-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="11803-108">EXAMPLES</span></span>

### <span data-ttu-id="11803-109">1:</span><span class="sxs-lookup"><span data-stu-id="11803-109">1:</span></span>
```
PS C:\>Remove-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="11803-110">Questo comando rimuove il backup con il backup con ID "12345" dall'app Web denominata WebAppStandard che appartiene al gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="11803-110">This command removes the backup with backup with ID of "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="11803-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="11803-111">PARAMETERS</span></span>

### <span data-ttu-id="11803-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="11803-112">-BackupId</span></span>
<span data-ttu-id="11803-113">ID backup</span><span class="sxs-lookup"><span data-stu-id="11803-113">Backup Id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11803-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11803-114">-DefaultProfile</span></span>
<span data-ttu-id="11803-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="11803-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11803-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="11803-116">-Name</span></span>
<span data-ttu-id="11803-117">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="11803-117">WebApp Name</span></span>

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

### <span data-ttu-id="11803-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11803-118">-ResourceGroupName</span></span>
<span data-ttu-id="11803-119">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="11803-119">Resource Group Name</span></span>

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

### <span data-ttu-id="11803-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="11803-120">-Slot</span></span>
<span data-ttu-id="11803-121">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="11803-121">WebApp Slot Name</span></span>

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

### <span data-ttu-id="11803-122">-Web App</span><span class="sxs-lookup"><span data-stu-id="11803-122">-WebApp</span></span>
<span data-ttu-id="11803-123">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="11803-123">WebApp Object</span></span>

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

### <span data-ttu-id="11803-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11803-124">CommonParameters</span></span>
<span data-ttu-id="11803-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11803-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11803-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11803-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11803-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="11803-127">INPUTS</span></span>

### <span data-ttu-id="11803-128">Sito</span><span class="sxs-lookup"><span data-stu-id="11803-128">Site</span></span>
<span data-ttu-id="11803-129">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="11803-129">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="11803-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="11803-130">OUTPUTS</span></span>

### <span data-ttu-id="11803-131">Microsoft. Azure. Management. website. Models. BackupItem</span><span class="sxs-lookup"><span data-stu-id="11803-131">Microsoft.Azure.Management.WebSites.Models.BackupItem</span></span>

## <span data-ttu-id="11803-132">Note</span><span class="sxs-lookup"><span data-stu-id="11803-132">NOTES</span></span>

## <span data-ttu-id="11803-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="11803-133">RELATED LINKS</span></span>

