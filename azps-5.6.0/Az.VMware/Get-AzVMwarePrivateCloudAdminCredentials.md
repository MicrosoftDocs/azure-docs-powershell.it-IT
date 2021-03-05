---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/get-azvmwareprivatecloudadmincredentials
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwarePrivateCloudAdminCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwarePrivateCloudAdminCredentials.md
ms.openlocfilehash: 88ecb5baff31ddcc27ce090f19a868c4d393c588
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987166"
---
# <span data-ttu-id="0c267-101">Get-AzVMWarePrivateCloudAdminCredentials</span><span class="sxs-lookup"><span data-stu-id="0c267-101">Get-AzVMWarePrivateCloudAdminCredentials</span></span>

## <span data-ttu-id="0c267-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c267-102">SYNOPSIS</span></span>
<span data-ttu-id="0c267-103">Elencare le credenziali di amministratore per il cloud privato</span><span class="sxs-lookup"><span data-stu-id="0c267-103">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="0c267-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0c267-104">SYNTAX</span></span>

```
Get-AzVMWarePrivateCloudAdminCredentials -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0c267-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0c267-105">DESCRIPTION</span></span>
<span data-ttu-id="0c267-106">Elencare le credenziali di amministratore per il cloud privato</span><span class="sxs-lookup"><span data-stu-id="0c267-106">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="0c267-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0c267-107">EXAMPLES</span></span>

### <span data-ttu-id="0c267-108">Esempio 1: Ottenere le credenziali di amministratore del cloud privato</span><span class="sxs-lookup"><span data-stu-id="0c267-108">Example 1: Get admin credential of private cloud</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloudAdminCredentials -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

NsxtPassword NsxtUsername VcenterPassword VcenterUsername
------------ ------------ --------------- ---------------
************ admin        ************    cloudadmin@vsphere.local
```

<span data-ttu-id="0c267-109">Ottenere le credenziali di amministratore del cloud privato</span><span class="sxs-lookup"><span data-stu-id="0c267-109">Get admin credential of private cloud</span></span>

## <span data-ttu-id="0c267-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c267-110">PARAMETERS</span></span>

### <span data-ttu-id="0c267-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c267-111">-DefaultProfile</span></span>
<span data-ttu-id="0c267-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0c267-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c267-113">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="0c267-113">-PrivateCloudName</span></span>
<span data-ttu-id="0c267-114">Nome del cloud privato</span><span class="sxs-lookup"><span data-stu-id="0c267-114">Name of the private cloud</span></span>

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

### <span data-ttu-id="0c267-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c267-115">-ResourceGroupName</span></span>
<span data-ttu-id="0c267-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0c267-116">The name of the resource group.</span></span>
<span data-ttu-id="0c267-117">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="0c267-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0c267-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0c267-118">-SubscriptionId</span></span>
<span data-ttu-id="0c267-119">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0c267-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0c267-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0c267-120">-Confirm</span></span>
<span data-ttu-id="0c267-121">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c267-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c267-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c267-122">-WhatIf</span></span>
<span data-ttu-id="0c267-123">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0c267-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c267-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0c267-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c267-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c267-125">CommonParameters</span></span>
<span data-ttu-id="0c267-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c267-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c267-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0c267-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c267-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="0c267-128">INPUTS</span></span>

## <span data-ttu-id="0c267-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0c267-129">OUTPUTS</span></span>

### <span data-ttu-id="0c267-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IAdminCredentials</span><span class="sxs-lookup"><span data-stu-id="0c267-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IAdminCredentials</span></span>

## <span data-ttu-id="0c267-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="0c267-131">NOTES</span></span>

<span data-ttu-id="0c267-132">ALIAS</span><span class="sxs-lookup"><span data-stu-id="0c267-132">ALIASES</span></span>

## <span data-ttu-id="0c267-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0c267-133">RELATED LINKS</span></span>

