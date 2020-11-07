---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
ms.openlocfilehash: 027e07ed495cb5b80fbd05852b640526c87bf16e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852382"
---
# <span data-ttu-id="3a548-101">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="3a548-101">Set-AzApiManagementGroup</span></span>

## <span data-ttu-id="3a548-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3a548-102">SYNOPSIS</span></span>
<span data-ttu-id="3a548-103">Configura un gruppo di gestione API.</span><span class="sxs-lookup"><span data-stu-id="3a548-103">Configures an API management group.</span></span>

## <span data-ttu-id="3a548-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3a548-104">SYNTAX</span></span>

```
Set-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a548-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a548-105">DESCRIPTION</span></span>
<span data-ttu-id="3a548-106">Il cmdlet **set-AzApiManagementGroup** configura un gruppo di gestione API.</span><span class="sxs-lookup"><span data-stu-id="3a548-106">The **Set-AzApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="3a548-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3a548-107">EXAMPLES</span></span>

### <span data-ttu-id="3a548-108">Esempio 1: configurare un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="3a548-108">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementGroup -Context $apimContext -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="3a548-109">Questo comando configura un gruppo di gestione denominato Group0001.</span><span class="sxs-lookup"><span data-stu-id="3a548-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="3a548-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3a548-110">PARAMETERS</span></span>

### <span data-ttu-id="3a548-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="3a548-111">-Context</span></span>
<span data-ttu-id="3a548-112">Specifica un'istanza di un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="3a548-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="3a548-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a548-113">-DefaultProfile</span></span>
<span data-ttu-id="3a548-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3a548-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a548-115">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a548-115">-Description</span></span>
<span data-ttu-id="3a548-116">Specifica la descrizione del gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="3a548-116">Specifies the description of the management group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a548-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="3a548-117">-GroupId</span></span>
<span data-ttu-id="3a548-118">Specifica l'identificatore del gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="3a548-118">Specifies the identifier of the management group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a548-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="3a548-119">-Name</span></span>
<span data-ttu-id="3a548-120">Specifica il nome del gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="3a548-120">Specifies the name of the management group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a548-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a548-121">-PassThru</span></span>
<span data-ttu-id="3a548-122">PassThru</span><span class="sxs-lookup"><span data-stu-id="3a548-122">passthru</span></span>

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

### <span data-ttu-id="3a548-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a548-123">CommonParameters</span></span>
<span data-ttu-id="3a548-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a548-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a548-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a548-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a548-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3a548-126">INPUTS</span></span>

### <span data-ttu-id="3a548-127">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3a548-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3a548-128">System. String</span><span class="sxs-lookup"><span data-stu-id="3a548-128">System.String</span></span>

### <span data-ttu-id="3a548-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3a548-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3a548-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3a548-130">OUTPUTS</span></span>

### <span data-ttu-id="3a548-131">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="3a548-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="3a548-132">Note</span><span class="sxs-lookup"><span data-stu-id="3a548-132">NOTES</span></span>

## <span data-ttu-id="3a548-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3a548-133">RELATED LINKS</span></span>

[<span data-ttu-id="3a548-134">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="3a548-134">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="3a548-135">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="3a548-135">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="3a548-136">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="3a548-136">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)


