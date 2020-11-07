---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 288EF15B-FE5C-44AE-ABD5-2B92F408B9EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantsyncstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
ms.openlocfilehash: a883da9c32c909801f9b7c1a795bd513ada737d8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673620"
---
# <span data-ttu-id="24c60-101">Get-AzApiManagementTenantSyncState</span><span class="sxs-lookup"><span data-stu-id="24c60-101">Get-AzApiManagementTenantSyncState</span></span>

## <span data-ttu-id="24c60-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="24c60-102">SYNOPSIS</span></span>
<span data-ttu-id="24c60-103">Ottiene lo stato della sincronizzazione più recente tra il database di configurazione e il repository git.</span><span class="sxs-lookup"><span data-stu-id="24c60-103">Gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="24c60-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="24c60-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantSyncState -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="24c60-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="24c60-105">DESCRIPTION</span></span>
<span data-ttu-id="24c60-106">Il cmdlet **Get-AzApiManagementTenantSyncState** ottiene lo stato della sincronizzazione più recente tra il database di configurazione e il repository git.</span><span class="sxs-lookup"><span data-stu-id="24c60-106">The **Get-AzApiManagementTenantSyncState** cmdlet gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="24c60-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="24c60-107">EXAMPLES</span></span>

### <span data-ttu-id="24c60-108">Esempio 1: ottenere lo stato della sincronizzazione più recente</span><span class="sxs-lookup"><span data-stu-id="24c60-108">Example 1: Get the status of the most recent synchronization</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantSyncState -Context $apimContext
```

<span data-ttu-id="24c60-109">Questo comando consente di ottenere lo stato della sincronizzazione più recente tra il database di configurazione e il repository git.</span><span class="sxs-lookup"><span data-stu-id="24c60-109">This command gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="24c60-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="24c60-110">PARAMETERS</span></span>

### <span data-ttu-id="24c60-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="24c60-111">-Context</span></span>
<span data-ttu-id="24c60-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="24c60-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24c60-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24c60-113">-DefaultProfile</span></span>
<span data-ttu-id="24c60-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="24c60-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24c60-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24c60-115">CommonParameters</span></span>
<span data-ttu-id="24c60-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24c60-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24c60-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24c60-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24c60-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="24c60-118">INPUTS</span></span>

### <span data-ttu-id="24c60-119">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="24c60-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="24c60-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="24c60-120">OUTPUTS</span></span>

### <span data-ttu-id="24c60-121">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementTenantConfigurationSyncState</span><span class="sxs-lookup"><span data-stu-id="24c60-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementTenantConfigurationSyncState</span></span>

## <span data-ttu-id="24c60-122">Note</span><span class="sxs-lookup"><span data-stu-id="24c60-122">NOTES</span></span>

## <span data-ttu-id="24c60-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="24c60-123">RELATED LINKS</span></span>