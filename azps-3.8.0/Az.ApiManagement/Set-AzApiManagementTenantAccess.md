---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 3B5FC8E3-5A02-4F3B-81F0-51DFE47A201B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementTenantAccess.md
ms.openlocfilehash: 08bbb81998107a11a5996cb75a6fba8b760802db
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022125"
---
# <span data-ttu-id="fdf58-101">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="fdf58-101">Set-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="fdf58-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fdf58-102">SYNOPSIS</span></span>
<span data-ttu-id="fdf58-103">Abilita o Disabilita l'accesso del tenant.</span><span class="sxs-lookup"><span data-stu-id="fdf58-103">Enables or disables tenant access.</span></span>

## <span data-ttu-id="fdf58-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fdf58-104">SYNTAX</span></span>

```
Set-AzApiManagementTenantAccess -Context <PsApiManagementContext> -Enabled <Boolean> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdf58-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fdf58-105">DESCRIPTION</span></span>
<span data-ttu-id="fdf58-106">Il cmdlet **set-AzApiManagementTenantAccess** Abilita o Disabilita l'accesso del tenant.</span><span class="sxs-lookup"><span data-stu-id="fdf58-106">The **Set-AzApiManagementTenantAccess** cmdlet enables or disables tenant access.</span></span>

## <span data-ttu-id="fdf58-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fdf58-107">EXAMPLES</span></span>

### <span data-ttu-id="fdf58-108">Esempio 1: abilitare l'accesso del tenant</span><span class="sxs-lookup"><span data-stu-id="fdf58-108">Example 1: Enable tenant access</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementTenantAccess -Context $apimContext -Enabled $True
```

<span data-ttu-id="fdf58-109">Questo comando consente l'accesso del tenant nel contesto specificato.</span><span class="sxs-lookup"><span data-stu-id="fdf58-109">This command enables tenant access in the specified context.</span></span>

## <span data-ttu-id="fdf58-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fdf58-110">PARAMETERS</span></span>

### <span data-ttu-id="fdf58-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="fdf58-111">-Context</span></span>
<span data-ttu-id="fdf58-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="fdf58-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="fdf58-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdf58-113">-DefaultProfile</span></span>
<span data-ttu-id="fdf58-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fdf58-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fdf58-115">-Enabled</span><span class="sxs-lookup"><span data-stu-id="fdf58-115">-Enabled</span></span>
<span data-ttu-id="fdf58-116">Specifica se questo cmdlet Abilita o Disabilita l'accesso del tenant.</span><span class="sxs-lookup"><span data-stu-id="fdf58-116">Specifies whether this cmdlet enables or disables tenant access.</span></span>
<span data-ttu-id="fdf58-117">Specificare un valore di $True per abilitare o $False per disabilitare.</span><span class="sxs-lookup"><span data-stu-id="fdf58-117">Specify a value of $True to enable or $False to disable.</span></span>

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

### <span data-ttu-id="fdf58-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fdf58-118">-PassThru</span></span>
<span data-ttu-id="fdf58-119">Indica che questo cmdlet restituisce il **PsApiManagementAccessInformation** modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fdf58-119">Indicates that this cmdlet returns the **PsApiManagementAccessInformation** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="fdf58-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdf58-120">CommonParameters</span></span>
<span data-ttu-id="fdf58-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdf58-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdf58-122">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fdf58-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdf58-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fdf58-123">INPUTS</span></span>

### <span data-ttu-id="fdf58-124">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="fdf58-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="fdf58-125">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fdf58-125">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fdf58-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fdf58-126">OUTPUTS</span></span>

### <span data-ttu-id="fdf58-127">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="fdf58-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="fdf58-128">Note</span><span class="sxs-lookup"><span data-stu-id="fdf58-128">NOTES</span></span>

## <span data-ttu-id="fdf58-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fdf58-129">RELATED LINKS</span></span>

[<span data-ttu-id="fdf58-130">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="fdf58-130">Get-AzApiManagementTenantAccess</span></span>](./Get-AzApiManagementTenantAccess.md)


