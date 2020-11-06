---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 3B5FC8E3-5A02-4F3B-81F0-51DFE47A201B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementTenantAccess.md
ms.openlocfilehash: c75aceee59e5696d928f19fa6d5ae317828fa82f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508784"
---
# <span data-ttu-id="5e37a-101">Set-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="5e37a-101">Set-AzureRmApiManagementTenantAccess</span></span>

## <span data-ttu-id="5e37a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5e37a-102">SYNOPSIS</span></span>
<span data-ttu-id="5e37a-103">Abilita o Disabilita l'accesso del tenant.</span><span class="sxs-lookup"><span data-stu-id="5e37a-103">Enables or disables tenant access.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e37a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5e37a-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementTenantAccess -Context <PsApiManagementContext> -Enabled <Boolean> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e37a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e37a-105">DESCRIPTION</span></span>
<span data-ttu-id="5e37a-106">Il cmdlet **set-AzureRmApiManagementTenantAccess** Abilita o Disabilita l'accesso del tenant.</span><span class="sxs-lookup"><span data-stu-id="5e37a-106">The **Set-AzureRmApiManagementTenantAccess** cmdlet enables or disables tenant access.</span></span>

## <span data-ttu-id="5e37a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5e37a-107">EXAMPLES</span></span>

### <span data-ttu-id="5e37a-108">Esempio 1: abilitare l'accesso del tenant</span><span class="sxs-lookup"><span data-stu-id="5e37a-108">Example 1: Enable tenant access</span></span>
```
PS C:\>Set-AzureRmApiManagementTenantAccess -Context $ApimContext -Enabled $True
```

<span data-ttu-id="5e37a-109">Questo comando consente l'accesso del tenant nel contesto specificato.</span><span class="sxs-lookup"><span data-stu-id="5e37a-109">This command enables tenant access in the specified context.</span></span>

## <span data-ttu-id="5e37a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5e37a-110">PARAMETERS</span></span>

### <span data-ttu-id="5e37a-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="5e37a-111">-Context</span></span>
<span data-ttu-id="5e37a-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="5e37a-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="5e37a-113">-Enabled</span><span class="sxs-lookup"><span data-stu-id="5e37a-113">-Enabled</span></span>
<span data-ttu-id="5e37a-114">Specifica se questo cmdlet Abilita o Disabilita l'accesso del tenant.</span><span class="sxs-lookup"><span data-stu-id="5e37a-114">Specifies whether this cmdlet enables or disables tenant access.</span></span>
<span data-ttu-id="5e37a-115">Specificare un valore di $True per abilitare o $False per disabilitare.</span><span class="sxs-lookup"><span data-stu-id="5e37a-115">Specify a value of $True to enable or $False to disable.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e37a-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5e37a-116">-PassThru</span></span>
<span data-ttu-id="5e37a-117">Indica che questo cmdlet restituisce il **PsApiManagementAccessInformation** modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e37a-117">Indicates that this cmdlet returns the **PsApiManagementAccessInformation** that this cmdlet modifies.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e37a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e37a-118">-DefaultProfile</span></span>
<span data-ttu-id="5e37a-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5e37a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e37a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e37a-120">CommonParameters</span></span>
<span data-ttu-id="5e37a-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e37a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e37a-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e37a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e37a-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5e37a-123">INPUTS</span></span>

## <span data-ttu-id="5e37a-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5e37a-124">OUTPUTS</span></span>

### <span data-ttu-id="5e37a-125">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="5e37a-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="5e37a-126">Note</span><span class="sxs-lookup"><span data-stu-id="5e37a-126">NOTES</span></span>

## <span data-ttu-id="5e37a-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5e37a-127">RELATED LINKS</span></span>

[<span data-ttu-id="5e37a-128">Get-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="5e37a-128">Get-AzureRmApiManagementTenantAccess</span></span>](./Get-AzureRmApiManagementTenantAccess.md)


