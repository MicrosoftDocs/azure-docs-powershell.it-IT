---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 3B5FC8E3-5A02-4F3B-81F0-51DFE47A201B
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementTenantAccess.md
ms.openlocfilehash: 1685b9607108fa0b7795fb0ed2c69eb94735fc5b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978958"
---
# <span data-ttu-id="179ac-101">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="179ac-101">Set-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="179ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="179ac-102">SYNOPSIS</span></span>
<span data-ttu-id="179ac-103">Abilita o disabilita l'accesso al tenant.</span><span class="sxs-lookup"><span data-stu-id="179ac-103">Enables or disables tenant access.</span></span>

## <span data-ttu-id="179ac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="179ac-104">SYNTAX</span></span>

```
Set-AzApiManagementTenantAccess -Context <PsApiManagementContext> -Enabled <Boolean> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="179ac-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="179ac-105">DESCRIPTION</span></span>
<span data-ttu-id="179ac-106">Il cmdlet **Set-AzApiManagementTenantAccess** abilita o disabilita l'accesso al tenant.</span><span class="sxs-lookup"><span data-stu-id="179ac-106">The **Set-AzApiManagementTenantAccess** cmdlet enables or disables tenant access.</span></span>

## <span data-ttu-id="179ac-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="179ac-107">EXAMPLES</span></span>

### <span data-ttu-id="179ac-108">Esempio 1: Abilitare l'accesso tenant</span><span class="sxs-lookup"><span data-stu-id="179ac-108">Example 1: Enable tenant access</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementTenantAccess -Context $apimContext -Enabled $True
```

<span data-ttu-id="179ac-109">Questo comando abilita l'accesso al tenant nel contesto specificato.</span><span class="sxs-lookup"><span data-stu-id="179ac-109">This command enables tenant access in the specified context.</span></span>

## <span data-ttu-id="179ac-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="179ac-110">PARAMETERS</span></span>

### <span data-ttu-id="179ac-111">-Context</span><span class="sxs-lookup"><span data-stu-id="179ac-111">-Context</span></span>
<span data-ttu-id="179ac-112">Specifica un **oggetto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="179ac-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="179ac-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="179ac-113">-DefaultProfile</span></span>
<span data-ttu-id="179ac-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="179ac-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="179ac-115">-Enabled</span><span class="sxs-lookup"><span data-stu-id="179ac-115">-Enabled</span></span>
<span data-ttu-id="179ac-116">Specifica se questo cmdlet abilita o disabilita l'accesso al tenant.</span><span class="sxs-lookup"><span data-stu-id="179ac-116">Specifies whether this cmdlet enables or disables tenant access.</span></span>
<span data-ttu-id="179ac-117">Specificare un valore di $True da abilitare o $False disattivare.</span><span class="sxs-lookup"><span data-stu-id="179ac-117">Specify a value of $True to enable or $False to disable.</span></span>

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

### <span data-ttu-id="179ac-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="179ac-118">-PassThru</span></span>
<span data-ttu-id="179ac-119">Indica che questo cmdlet restituisce **PsApiManagementAccessInformation** che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="179ac-119">Indicates that this cmdlet returns the **PsApiManagementAccessInformation** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="179ac-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="179ac-120">CommonParameters</span></span>
<span data-ttu-id="179ac-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="179ac-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="179ac-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="179ac-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="179ac-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="179ac-123">INPUTS</span></span>

### <span data-ttu-id="179ac-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="179ac-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="179ac-125">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="179ac-125">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="179ac-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="179ac-126">OUTPUTS</span></span>

### <span data-ttu-id="179ac-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="179ac-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="179ac-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="179ac-128">NOTES</span></span>

## <span data-ttu-id="179ac-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="179ac-129">RELATED LINKS</span></span>

[<span data-ttu-id="179ac-130">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="179ac-130">Get-AzApiManagementTenantAccess</span></span>](./Get-AzApiManagementTenantAccess.md)


