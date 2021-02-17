---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareprivatecloudadmincredentials
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwarePrivateCloudAdminCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwarePrivateCloudAdminCredentials.md
ms.openlocfilehash: 7502bbd96371aa505d8d927dfb9a491c2ca32b34
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207514"
---
# <span data-ttu-id="c8946-101">Get-AzVMwarePrivateCloudAdminCredentials</span><span class="sxs-lookup"><span data-stu-id="c8946-101">Get-AzVMwarePrivateCloudAdminCredentials</span></span>

## <span data-ttu-id="c8946-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8946-102">SYNOPSIS</span></span>
<span data-ttu-id="c8946-103">Elencare le credenziali di amministratore per il cloud privato</span><span class="sxs-lookup"><span data-stu-id="c8946-103">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="c8946-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c8946-104">SYNTAX</span></span>

```
Get-AzVMwarePrivateCloudAdminCredentials -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c8946-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c8946-105">DESCRIPTION</span></span>
<span data-ttu-id="c8946-106">Elencare le credenziali di amministratore per il cloud privato</span><span class="sxs-lookup"><span data-stu-id="c8946-106">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="c8946-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c8946-107">EXAMPLES</span></span>

### <span data-ttu-id="c8946-108">Esempio 1: Ottenere le credenziali di amministratore del cloud privato</span><span class="sxs-lookup"><span data-stu-id="c8946-108">Example 1: Get admin credential of private cloud</span></span>
```powershell
PS C:\> Get-AzVMwarePrivateCloudAdminCredentials -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

NsxtPassword NsxtUsername VcenterPassword VcenterUsername
------------ ------------ --------------- ---------------
************ admin        ************    cloudadmin@vsphere.local
```

<span data-ttu-id="c8946-109">Ottenere le credenziali di amministratore del cloud privato</span><span class="sxs-lookup"><span data-stu-id="c8946-109">Get admin credential of private cloud</span></span>

## <span data-ttu-id="c8946-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8946-110">PARAMETERS</span></span>

### <span data-ttu-id="c8946-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8946-111">-DefaultProfile</span></span>
<span data-ttu-id="c8946-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c8946-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8946-113">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="c8946-113">-PrivateCloudName</span></span>
<span data-ttu-id="c8946-114">Nome del cloud privato</span><span class="sxs-lookup"><span data-stu-id="c8946-114">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8946-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8946-115">-ResourceGroupName</span></span>
<span data-ttu-id="c8946-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c8946-116">The name of the resource group.</span></span>
<span data-ttu-id="c8946-117">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="c8946-117">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8946-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c8946-118">-SubscriptionId</span></span>
<span data-ttu-id="c8946-119">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c8946-119">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8946-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c8946-120">-Confirm</span></span>
<span data-ttu-id="c8946-121">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8946-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8946-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8946-122">-WhatIf</span></span>
<span data-ttu-id="c8946-123">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c8946-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8946-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c8946-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8946-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8946-125">CommonParameters</span></span>
<span data-ttu-id="c8946-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8946-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8946-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c8946-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8946-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="c8946-128">INPUTS</span></span>

## <span data-ttu-id="c8946-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c8946-129">OUTPUTS</span></span>

### <span data-ttu-id="c8946-130">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IAdminCredentials</span><span class="sxs-lookup"><span data-stu-id="c8946-130">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IAdminCredentials</span></span>

## <span data-ttu-id="c8946-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="c8946-131">NOTES</span></span>

<span data-ttu-id="c8946-132">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c8946-132">ALIASES</span></span>

## <span data-ttu-id="c8946-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c8946-133">RELATED LINKS</span></span>

