---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 288EF15B-FE5C-44AE-ABD5-2B92F408B9EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantsyncstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
ms.openlocfilehash: 233c74e3939884cd4bd311ec463d81d7e7613f31
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192510"
---
# <span data-ttu-id="9b276-101">Get-AzApiManagementTenantSyncState</span><span class="sxs-lookup"><span data-stu-id="9b276-101">Get-AzApiManagementTenantSyncState</span></span>

## <span data-ttu-id="9b276-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b276-102">SYNOPSIS</span></span>
<span data-ttu-id="9b276-103">Ottiene lo stato della sincronizzazione più recente tra il database di configurazione e il repository Git.</span><span class="sxs-lookup"><span data-stu-id="9b276-103">Gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="9b276-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9b276-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantSyncState -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9b276-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9b276-105">DESCRIPTION</span></span>
<span data-ttu-id="9b276-106">Il cmdlet **Get-AzApiManagementTenantSyncState** ottiene lo stato della sincronizzazione più recente tra il database di configurazione e il repository Git.</span><span class="sxs-lookup"><span data-stu-id="9b276-106">The **Get-AzApiManagementTenantSyncState** cmdlet gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="9b276-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9b276-107">EXAMPLES</span></span>

### <span data-ttu-id="9b276-108">Esempio 1: Ottenere lo stato della sincronizzazione più recente</span><span class="sxs-lookup"><span data-stu-id="9b276-108">Example 1: Get the status of the most recent synchronization</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantSyncState -Context $apimContext
```

<span data-ttu-id="9b276-109">Questo comando recupera lo stato della sincronizzazione più recente tra il database di configurazione e il repository Git.</span><span class="sxs-lookup"><span data-stu-id="9b276-109">This command gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="9b276-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b276-110">PARAMETERS</span></span>

### <span data-ttu-id="9b276-111">-Context</span><span class="sxs-lookup"><span data-stu-id="9b276-111">-Context</span></span>
<span data-ttu-id="9b276-112">Specifica un **oggetto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="9b276-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="9b276-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b276-113">-DefaultProfile</span></span>
<span data-ttu-id="9b276-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9b276-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b276-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b276-115">CommonParameters</span></span>
<span data-ttu-id="9b276-116">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b276-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b276-117">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9b276-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b276-118">INPUT</span><span class="sxs-lookup"><span data-stu-id="9b276-118">INPUTS</span></span>

### <span data-ttu-id="9b276-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9b276-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="9b276-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9b276-120">OUTPUTS</span></span>

### <span data-ttu-id="9b276-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementTenantConfigurationSyncState</span><span class="sxs-lookup"><span data-stu-id="9b276-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementTenantConfigurationSyncState</span></span>

## <span data-ttu-id="9b276-122">NOTE</span><span class="sxs-lookup"><span data-stu-id="9b276-122">NOTES</span></span>

## <span data-ttu-id="9b276-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9b276-123">RELATED LINKS</span></span>
