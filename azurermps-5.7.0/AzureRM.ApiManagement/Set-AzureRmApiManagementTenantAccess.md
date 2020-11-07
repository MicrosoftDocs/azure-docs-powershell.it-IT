---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 3B5FC8E3-5A02-4F3B-81F0-51DFE47A201B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementTenantAccess.md
ms.openlocfilehash: 55158ac4f6489d70e17008c9e8c4ef13bd6d4fe0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688196"
---
# <span data-ttu-id="5a634-101">Set-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="5a634-101">Set-AzureRmApiManagementTenantAccess</span></span>

## <span data-ttu-id="5a634-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5a634-102">SYNOPSIS</span></span>
<span data-ttu-id="5a634-103">Abilita o Disabilita l'accesso del tenant.</span><span class="sxs-lookup"><span data-stu-id="5a634-103">Enables or disables tenant access.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a634-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5a634-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementTenantAccess -Context <PsApiManagementContext> -Enabled <Boolean> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a634-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5a634-105">DESCRIPTION</span></span>
<span data-ttu-id="5a634-106">Il cmdlet **set-AzureRmApiManagementTenantAccess** Abilita o Disabilita l'accesso del tenant.</span><span class="sxs-lookup"><span data-stu-id="5a634-106">The **Set-AzureRmApiManagementTenantAccess** cmdlet enables or disables tenant access.</span></span>

## <span data-ttu-id="5a634-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5a634-107">EXAMPLES</span></span>

### <span data-ttu-id="5a634-108">Esempio 1: abilitare l'accesso del tenant</span><span class="sxs-lookup"><span data-stu-id="5a634-108">Example 1: Enable tenant access</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementTenantAccess -Context $apimContext -Enabled $True
```

<span data-ttu-id="5a634-109">Questo comando consente l'accesso del tenant nel contesto specificato.</span><span class="sxs-lookup"><span data-stu-id="5a634-109">This command enables tenant access in the specified context.</span></span>

## <span data-ttu-id="5a634-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5a634-110">PARAMETERS</span></span>

### <span data-ttu-id="5a634-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="5a634-111">-Context</span></span>
<span data-ttu-id="5a634-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="5a634-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="5a634-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a634-113">-DefaultProfile</span></span>
<span data-ttu-id="5a634-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5a634-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="5a634-115">-Enabled</span><span class="sxs-lookup"><span data-stu-id="5a634-115">-Enabled</span></span>
<span data-ttu-id="5a634-116">Specifica se questo cmdlet Abilita o Disabilita l'accesso del tenant.</span><span class="sxs-lookup"><span data-stu-id="5a634-116">Specifies whether this cmdlet enables or disables tenant access.</span></span>
<span data-ttu-id="5a634-117">Specificare un valore di $True per abilitare o $False per disabilitare.</span><span class="sxs-lookup"><span data-stu-id="5a634-117">Specify a value of $True to enable or $False to disable.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a634-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a634-118">-PassThru</span></span>
<span data-ttu-id="5a634-119">Indica che questo cmdlet restituisce il **PsApiManagementAccessInformation** modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a634-119">Indicates that this cmdlet returns the **PsApiManagementAccessInformation** that this cmdlet modifies.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a634-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a634-120">CommonParameters</span></span>
<span data-ttu-id="5a634-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a634-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a634-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a634-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a634-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5a634-123">INPUTS</span></span>

### <span data-ttu-id="5a634-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5a634-124">None</span></span>
<span data-ttu-id="5a634-125">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="5a634-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5a634-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5a634-126">OUTPUTS</span></span>

### <span data-ttu-id="5a634-127">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="5a634-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="5a634-128">Note</span><span class="sxs-lookup"><span data-stu-id="5a634-128">NOTES</span></span>

## <span data-ttu-id="5a634-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5a634-129">RELATED LINKS</span></span>

[<span data-ttu-id="5a634-130">Get-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="5a634-130">Get-AzureRmApiManagementTenantAccess</span></span>](./Get-AzureRmApiManagementTenantAccess.md)


