---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappsnapshot
schema: 2.0.0
ms.openlocfilehash: 754ff798ca001e2c6b5a067f6e6244704fc2f617
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865871"
---
# <span data-ttu-id="52b56-101">Get-AzureRmWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="52b56-101">Get-AzureRmWebAppSnapshot</span></span>

## <span data-ttu-id="52b56-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="52b56-102">SYNOPSIS</span></span>
<span data-ttu-id="52b56-103">Ottiene gli snapshot disponibili per un'app Web.</span><span class="sxs-lookup"><span data-stu-id="52b56-103">Gets the snapshots available for a web app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52b56-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="52b56-104">SYNTAX</span></span>

### <span data-ttu-id="52b56-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="52b56-105">FromResourceName</span></span>
```
Get-AzureRmWebAppSnapshot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="52b56-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="52b56-106">FromWebApp</span></span>
```
Get-AzureRmWebAppSnapshot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="52b56-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="52b56-107">DESCRIPTION</span></span>
<span data-ttu-id="52b56-108">Il cmdlet **Get-AzureRmWebAppSnapshot** restituisce tutti gli snapshot per un'app Web.</span><span class="sxs-lookup"><span data-stu-id="52b56-108">The **Get-AzureRmWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="52b56-109">Gli snapshot sono backup automatici dei file e delle impostazioni di un'app Web.</span><span class="sxs-lookup"><span data-stu-id="52b56-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="52b56-110">Uno snapshot può essere ripristinato con il cmdlet **Restore-AzureRmWebAppSnapshot** .</span><span class="sxs-lookup"><span data-stu-id="52b56-110">A snapshot can be restored with the **Restore-AzureRmWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="52b56-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="52b56-111">EXAMPLES</span></span>

### <span data-ttu-id="52b56-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="52b56-112">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="52b56-113">Ottenere gli snapshot per un'app Web denominata "ConstosoApp" con uno slot denominato "Staging" nel gruppo di risorse "predefinito-Web-Westus"</span><span class="sxs-lookup"><span data-stu-id="52b56-113">Get the snapshots for a web app named "ConstosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="52b56-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="52b56-114">PARAMETERS</span></span>

### <span data-ttu-id="52b56-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52b56-115">-DefaultProfile</span></span>
<span data-ttu-id="52b56-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="52b56-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52b56-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="52b56-117">-Name</span></span>
<span data-ttu-id="52b56-118">Nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="52b56-118">The name of the web app.</span></span>

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

### <span data-ttu-id="52b56-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52b56-119">-ResourceGroupName</span></span>
<span data-ttu-id="52b56-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="52b56-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="52b56-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="52b56-121">-Slot</span></span>
<span data-ttu-id="52b56-122">Il nome dello slot Web App.</span><span class="sxs-lookup"><span data-stu-id="52b56-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="52b56-123">-Web App</span><span class="sxs-lookup"><span data-stu-id="52b56-123">-WebApp</span></span>
<span data-ttu-id="52b56-124">Oggetto app Web</span><span class="sxs-lookup"><span data-stu-id="52b56-124">The web app object</span></span>

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

## <span data-ttu-id="52b56-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="52b56-125">INPUTS</span></span>

### <span data-ttu-id="52b56-126">System. String</span><span class="sxs-lookup"><span data-stu-id="52b56-126">System.String</span></span>
<span data-ttu-id="52b56-127">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="52b56-127">Microsoft.Azure.Management.WebSites.Models.Site</span></span>


## <span data-ttu-id="52b56-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="52b56-128">OUTPUTS</span></span>

### <span data-ttu-id="52b56-129">Microsoft. Azure. Commands. webapps. Cmdlets. BackupRestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="52b56-129">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>


## <span data-ttu-id="52b56-130">Note</span><span class="sxs-lookup"><span data-stu-id="52b56-130">NOTES</span></span>

## <span data-ttu-id="52b56-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="52b56-131">RELATED LINKS</span></span>

