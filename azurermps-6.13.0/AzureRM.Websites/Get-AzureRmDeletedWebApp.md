---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmDeletedWebApp.md
ms.openlocfilehash: 75ad4e1fabb511ee4ca3cff024389a8e826aeadd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516336"
---
# <span data-ttu-id="4fb6c-101">Get-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="4fb6c-101">Get-AzureRmDeletedWebApp</span></span>

## <span data-ttu-id="4fb6c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4fb6c-102">SYNOPSIS</span></span>
<span data-ttu-id="4fb6c-103">Ottiene le app Web eliminate nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4fb6c-103">Gets deleted web apps in the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fb6c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4fb6c-104">SYNTAX</span></span>

```
Get-AzureRmDeletedWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fb6c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4fb6c-105">DESCRIPTION</span></span>
<span data-ttu-id="4fb6c-106">Il cmdlet **Get-AzureRmDeletedWebApp** restituisce tutte le app Web eliminate nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4fb6c-106">The **Get-AzureRmDeletedWebApp** cmdlet returns all deleted web apps in the subscription.</span></span> <span data-ttu-id="4fb6c-107">Le app eliminate possono essere filtrate facoltativamente dal gruppo di risorse, dal nome e dallo slot.</span><span class="sxs-lookup"><span data-stu-id="4fb6c-107">Deleted apps can optionally be filtered by resource group, name, and slot.</span></span> <span data-ttu-id="4fb6c-108">Può essere presente più di un'app eliminata con lo stesso nome e il relativo gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4fb6c-108">There can be more than one deleted app with the same name and resource group.</span></span> <span data-ttu-id="4fb6c-109">Selezionare la DeletionTime per distinguere le app eliminate che condividono lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="4fb6c-109">Check the DeletionTime to distinguish deleted apps that share the same name.</span></span>

## <span data-ttu-id="4fb6c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4fb6c-110">EXAMPLES</span></span>

### <span data-ttu-id="4fb6c-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4fb6c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeletedWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="4fb6c-112">Questo comando consente di ottenere le app eliminate denominate ContosoSite appartenenti al gruppo di risorse default-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="4fb6c-112">This command gets the deleted apps named ContosoSite belonging to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="4fb6c-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4fb6c-113">PARAMETERS</span></span>

### <span data-ttu-id="4fb6c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fb6c-114">-DefaultProfile</span></span>
<span data-ttu-id="4fb6c-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4fb6c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fb6c-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="4fb6c-116">-Name</span></span>
<span data-ttu-id="4fb6c-117">Nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="4fb6c-117">The name of the web app.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fb6c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fb6c-118">-ResourceGroupName</span></span>
<span data-ttu-id="4fb6c-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4fb6c-119">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fb6c-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="4fb6c-120">-Slot</span></span>
<span data-ttu-id="4fb6c-121">Il nome dello slot Web App.</span><span class="sxs-lookup"><span data-stu-id="4fb6c-121">The name of the web app slot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fb6c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fb6c-122">CommonParameters</span></span>
<span data-ttu-id="4fb6c-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fb6c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4fb6c-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fb6c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fb6c-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4fb6c-125">INPUTS</span></span>

### <span data-ttu-id="4fb6c-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4fb6c-126">None</span></span>

## <span data-ttu-id="4fb6c-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4fb6c-127">OUTPUTS</span></span>

### <span data-ttu-id="4fb6c-128">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="4fb6c-128">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="4fb6c-129">Note</span><span class="sxs-lookup"><span data-stu-id="4fb6c-129">NOTES</span></span>

## <span data-ttu-id="4fb6c-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4fb6c-130">RELATED LINKS</span></span>

[<span data-ttu-id="4fb6c-131">Ripristinare-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="4fb6c-131">Restore-AzureRmDeletedWebApp</span></span>](./Restore-AzureRmDeletedWebApp.md)
