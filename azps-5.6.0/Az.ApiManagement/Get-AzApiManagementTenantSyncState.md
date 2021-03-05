---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 288EF15B-FE5C-44AE-ABD5-2B92F408B9EB
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementtenantsyncstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
ms.openlocfilehash: d253c1da05bd62e40dcdddaa90033512b3932d27
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004862"
---
# <span data-ttu-id="30af3-101">Get-AzApiManagementTenantSyncState</span><span class="sxs-lookup"><span data-stu-id="30af3-101">Get-AzApiManagementTenantSyncState</span></span>

## <span data-ttu-id="30af3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30af3-102">SYNOPSIS</span></span>
<span data-ttu-id="30af3-103">Ottiene lo stato della sincronizzazione più recente tra il database di configurazione e il repository Git.</span><span class="sxs-lookup"><span data-stu-id="30af3-103">Gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="30af3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="30af3-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantSyncState -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="30af3-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="30af3-105">DESCRIPTION</span></span>
<span data-ttu-id="30af3-106">Il cmdlet **Get-AzApiManagementTenantSyncState** ottiene lo stato della sincronizzazione più recente tra il database di configurazione e il repository Git.</span><span class="sxs-lookup"><span data-stu-id="30af3-106">The **Get-AzApiManagementTenantSyncState** cmdlet gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="30af3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="30af3-107">EXAMPLES</span></span>

### <span data-ttu-id="30af3-108">Esempio 1: Ottenere lo stato della sincronizzazione più recente</span><span class="sxs-lookup"><span data-stu-id="30af3-108">Example 1: Get the status of the most recent synchronization</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantSyncState -Context $apimContext
```

<span data-ttu-id="30af3-109">Questo comando recupera lo stato della sincronizzazione più recente tra il database di configurazione e il repository Git.</span><span class="sxs-lookup"><span data-stu-id="30af3-109">This command gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="30af3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30af3-110">PARAMETERS</span></span>

### <span data-ttu-id="30af3-111">-Context</span><span class="sxs-lookup"><span data-stu-id="30af3-111">-Context</span></span>
<span data-ttu-id="30af3-112">Specifica un **oggetto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="30af3-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30af3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30af3-113">-DefaultProfile</span></span>
<span data-ttu-id="30af3-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="30af3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30af3-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30af3-115">CommonParameters</span></span>
<span data-ttu-id="30af3-116">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30af3-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30af3-117">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="30af3-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30af3-118">INPUT</span><span class="sxs-lookup"><span data-stu-id="30af3-118">INPUTS</span></span>

### <span data-ttu-id="30af3-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="30af3-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="30af3-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="30af3-120">OUTPUTS</span></span>

### <span data-ttu-id="30af3-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementTenantConfigurationSyncState</span><span class="sxs-lookup"><span data-stu-id="30af3-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementTenantConfigurationSyncState</span></span>

## <span data-ttu-id="30af3-122">NOTE</span><span class="sxs-lookup"><span data-stu-id="30af3-122">NOTES</span></span>

## <span data-ttu-id="30af3-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="30af3-123">RELATED LINKS</span></span>
