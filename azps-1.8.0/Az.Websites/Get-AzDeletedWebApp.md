---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
ms.openlocfilehash: fabbaf6e34a39767c9ca0acdadd3fdc05d8e260f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676326"
---
# <span data-ttu-id="455f2-101">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="455f2-101">Get-AzDeletedWebApp</span></span>

## <span data-ttu-id="455f2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="455f2-102">SYNOPSIS</span></span>
<span data-ttu-id="455f2-103">Ottiene le app Web eliminate nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="455f2-103">Gets deleted web apps in the subscription.</span></span>

## <span data-ttu-id="455f2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="455f2-104">SYNTAX</span></span>

```
Get-AzDeletedWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="455f2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="455f2-105">DESCRIPTION</span></span>
<span data-ttu-id="455f2-106">Il cmdlet **Get-AzDeletedWebApp** restituisce tutte le app Web eliminate nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="455f2-106">The **Get-AzDeletedWebApp** cmdlet returns all deleted web apps in the subscription.</span></span> <span data-ttu-id="455f2-107">Le app eliminate possono essere filtrate facoltativamente dal gruppo di risorse, dal nome e dallo slot.</span><span class="sxs-lookup"><span data-stu-id="455f2-107">Deleted apps can optionally be filtered by resource group, name, and slot.</span></span> <span data-ttu-id="455f2-108">Può essere presente più di un'app eliminata con lo stesso nome e il relativo gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="455f2-108">There can be more than one deleted app with the same name and resource group.</span></span> <span data-ttu-id="455f2-109">Selezionare la DeletionTime per distinguere le app eliminate che condividono lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="455f2-109">Check the DeletionTime to distinguish deleted apps that share the same name.</span></span>

## <span data-ttu-id="455f2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="455f2-110">EXAMPLES</span></span>

### <span data-ttu-id="455f2-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="455f2-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeletedWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="455f2-112">Questo comando consente di ottenere le app eliminate denominate ContosoSite appartenenti al gruppo di risorse default-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="455f2-112">This command gets the deleted apps named ContosoSite belonging to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="455f2-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="455f2-113">PARAMETERS</span></span>

### <span data-ttu-id="455f2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="455f2-114">-DefaultProfile</span></span>
<span data-ttu-id="455f2-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="455f2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="455f2-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="455f2-116">-Name</span></span>
<span data-ttu-id="455f2-117">Nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="455f2-117">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="455f2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="455f2-118">-ResourceGroupName</span></span>
<span data-ttu-id="455f2-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="455f2-119">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="455f2-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="455f2-120">-Slot</span></span>
<span data-ttu-id="455f2-121">Il nome dello slot Web App.</span><span class="sxs-lookup"><span data-stu-id="455f2-121">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="455f2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="455f2-122">CommonParameters</span></span>
<span data-ttu-id="455f2-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="455f2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="455f2-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="455f2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="455f2-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="455f2-125">INPUTS</span></span>

### <span data-ttu-id="455f2-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="455f2-126">None</span></span>

## <span data-ttu-id="455f2-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="455f2-127">OUTPUTS</span></span>

### <span data-ttu-id="455f2-128">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="455f2-128">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="455f2-129">Note</span><span class="sxs-lookup"><span data-stu-id="455f2-129">NOTES</span></span>

## <span data-ttu-id="455f2-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="455f2-130">RELATED LINKS</span></span>

[<span data-ttu-id="455f2-131">Ripristinare-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="455f2-131">Restore-AzDeletedWebApp</span></span>](./Restore-AzDeletedWebApp.md)