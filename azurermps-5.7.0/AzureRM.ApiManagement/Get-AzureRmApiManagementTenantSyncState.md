---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 288EF15B-FE5C-44AE-ABD5-2B92F408B9EB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementtenantsyncstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantSyncState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantSyncState.md
ms.openlocfilehash: 64e1d8ad070d4ce1c2f8129a73efd8730f26d1a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514587"
---
# <span data-ttu-id="f1298-101">Get-AzureRmApiManagementTenantSyncState</span><span class="sxs-lookup"><span data-stu-id="f1298-101">Get-AzureRmApiManagementTenantSyncState</span></span>

## <span data-ttu-id="f1298-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f1298-102">SYNOPSIS</span></span>
<span data-ttu-id="f1298-103">Ottiene lo stato della sincronizzazione più recente tra il database di configurazione e il repository git.</span><span class="sxs-lookup"><span data-stu-id="f1298-103">Gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1298-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f1298-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementTenantSyncState -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1298-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1298-105">DESCRIPTION</span></span>
<span data-ttu-id="f1298-106">Il cmdlet **Get-AzureRmApiManagementTenantSyncState** ottiene lo stato della sincronizzazione più recente tra il database di configurazione e il repository git.</span><span class="sxs-lookup"><span data-stu-id="f1298-106">The **Get-AzureRmApiManagementTenantSyncState** cmdlet gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="f1298-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f1298-107">EXAMPLES</span></span>

### <span data-ttu-id="f1298-108">Esempio 1: ottenere lo stato della sincronizzazione più recente</span><span class="sxs-lookup"><span data-stu-id="f1298-108">Example 1: Get the status of the most recent synchronization</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementTenantSyncState -Context $apimContext 
```

<span data-ttu-id="f1298-109">Questo comando consente di ottenere lo stato della sincronizzazione più recente tra il database di configurazione e il repository git.</span><span class="sxs-lookup"><span data-stu-id="f1298-109">This command gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="f1298-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f1298-110">PARAMETERS</span></span>

### <span data-ttu-id="f1298-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="f1298-111">-Context</span></span>
<span data-ttu-id="f1298-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="f1298-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1298-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1298-113">-DefaultProfile</span></span>
<span data-ttu-id="f1298-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f1298-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="f1298-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1298-115">CommonParameters</span></span>
<span data-ttu-id="f1298-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1298-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1298-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1298-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1298-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f1298-118">INPUTS</span></span>

### <span data-ttu-id="f1298-119">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f1298-119">None</span></span>
<span data-ttu-id="f1298-120">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="f1298-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f1298-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f1298-121">OUTPUTS</span></span>

### <span data-ttu-id="f1298-122">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="f1298-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="f1298-123">Note</span><span class="sxs-lookup"><span data-stu-id="f1298-123">NOTES</span></span>

## <span data-ttu-id="f1298-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f1298-124">RELATED LINKS</span></span>

