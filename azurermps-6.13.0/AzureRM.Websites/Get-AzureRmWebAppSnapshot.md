---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSnapshot.md
ms.openlocfilehash: 292364ae6355c640ed66116c84289fe303acdd53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507244"
---
# <span data-ttu-id="52adb-101">Get-AzureRmWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="52adb-101">Get-AzureRmWebAppSnapshot</span></span>

## <span data-ttu-id="52adb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="52adb-102">SYNOPSIS</span></span>
<span data-ttu-id="52adb-103">Ottiene gli snapshot disponibili per un'app Web.</span><span class="sxs-lookup"><span data-stu-id="52adb-103">Gets the snapshots available for a web app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52adb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="52adb-104">SYNTAX</span></span>

### <span data-ttu-id="52adb-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="52adb-105">FromResourceName</span></span>
```
Get-AzureRmWebAppSnapshot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52adb-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="52adb-106">FromWebApp</span></span>
```
Get-AzureRmWebAppSnapshot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52adb-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="52adb-107">DESCRIPTION</span></span>
<span data-ttu-id="52adb-108">Il cmdlet **Get-AzureRmWebAppSnapshot** restituisce tutti gli snapshot per un'app Web.</span><span class="sxs-lookup"><span data-stu-id="52adb-108">The **Get-AzureRmWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="52adb-109">Gli snapshot sono backup automatici dei file e delle impostazioni di un'app Web.</span><span class="sxs-lookup"><span data-stu-id="52adb-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="52adb-110">Uno snapshot può essere ripristinato con il cmdlet **Restore-AzureRmWebAppSnapshot** .</span><span class="sxs-lookup"><span data-stu-id="52adb-110">A snapshot can be restored with the **Restore-AzureRmWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="52adb-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="52adb-111">EXAMPLES</span></span>

### <span data-ttu-id="52adb-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="52adb-112">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="52adb-113">Ottenere gli snapshot per un'app Web denominata "ConstosoApp" con uno slot denominato "Staging" nel gruppo di risorse "predefinito-Web-Westus"</span><span class="sxs-lookup"><span data-stu-id="52adb-113">Get the snapshots for a web app named "ConstosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="52adb-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="52adb-114">PARAMETERS</span></span>

### <span data-ttu-id="52adb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52adb-115">-DefaultProfile</span></span>
<span data-ttu-id="52adb-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="52adb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52adb-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="52adb-117">-Name</span></span>
<span data-ttu-id="52adb-118">Nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="52adb-118">The name of the web app.</span></span>

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

### <span data-ttu-id="52adb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52adb-119">-ResourceGroupName</span></span>
<span data-ttu-id="52adb-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="52adb-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="52adb-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="52adb-121">-Slot</span></span>
<span data-ttu-id="52adb-122">Il nome dello slot Web App.</span><span class="sxs-lookup"><span data-stu-id="52adb-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="52adb-123">-Web App</span><span class="sxs-lookup"><span data-stu-id="52adb-123">-WebApp</span></span>
<span data-ttu-id="52adb-124">Oggetto app Web</span><span class="sxs-lookup"><span data-stu-id="52adb-124">The web app object</span></span>

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

### <span data-ttu-id="52adb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52adb-125">CommonParameters</span></span>
<span data-ttu-id="52adb-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52adb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52adb-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52adb-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52adb-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="52adb-128">INPUTS</span></span>

### <span data-ttu-id="52adb-129">System. String</span><span class="sxs-lookup"><span data-stu-id="52adb-129">System.String</span></span>

### <span data-ttu-id="52adb-130">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="52adb-130">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="52adb-131">Parametri: Web App (ByValue)</span><span class="sxs-lookup"><span data-stu-id="52adb-131">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="52adb-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="52adb-132">OUTPUTS</span></span>

### <span data-ttu-id="52adb-133">Microsoft. Azure. Commands. webapps. Cmdlets. BackupRestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="52adb-133">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="52adb-134">Note</span><span class="sxs-lookup"><span data-stu-id="52adb-134">NOTES</span></span>

## <span data-ttu-id="52adb-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="52adb-135">RELATED LINKS</span></span>
