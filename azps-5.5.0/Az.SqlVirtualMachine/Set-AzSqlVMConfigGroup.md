---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/set-azsqlvmconfiggroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Set-AzSqlVMConfigGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Set-AzSqlVMConfigGroup.md
ms.openlocfilehash: b83dc58161791009a3adfd7cbf9b0b07b3f0b5b1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176694"
---
# <span data-ttu-id="28a51-101">Set-AzSqlVMConfigGroup</span><span class="sxs-lookup"><span data-stu-id="28a51-101">Set-AzSqlVMConfigGroup</span></span>

## <span data-ttu-id="28a51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28a51-102">SYNOPSIS</span></span>
<span data-ttu-id="28a51-103">Impostare le informazioni relative a un gruppo di macchine virtuali SQL in una configurazione di macchine virtuali SQL.</span><span class="sxs-lookup"><span data-stu-id="28a51-103">Set the information relative to a sql virtual machine group in a sql virtual machine configuration.</span></span>

## <span data-ttu-id="28a51-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="28a51-104">SYNTAX</span></span>

```
Set-AzSqlVMConfigGroup [-SqlVM] <AzureSqlVMModel> [-SqlVMGroup] <AzureSqlVMGroupModel>
 -ClusterOperatorAccountPassword <SecureString> -SqlServiceAccountPassword <SecureString>
 [-ClusterBootstrapAccountPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="28a51-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="28a51-105">DESCRIPTION</span></span>
<span data-ttu-id="28a51-106">Il Set-AzSqlVMConfigGroup cmdlet imposta le informazioni necessarie per partecipare a un gruppo di macchine virtuali SQL per la configurazione di una macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="28a51-106">The Set-AzSqlVMConfigGroup cmdlet set the information needed in order to join a sql virtual machine group for a sql virtual machine configuration.</span></span>

## <span data-ttu-id="28a51-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="28a51-107">EXAMPLES</span></span>

### <span data-ttu-id="28a51-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="28a51-108">Example 1</span></span>
```powershell
PS C:\> $config = Set-AzSqlVMConfigGroup -SqlVM $config -SqlVMGroup $group -ClusterOperatorAccountPassword 'password' -SqlServiceAccountPassword 'password'
```

<span data-ttu-id="28a51-109">Aggiornare le informazioni sul gruppo di una configurazione di macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="28a51-109">Update the group informations of a sql virtual machine configuration.</span></span>

## <span data-ttu-id="28a51-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28a51-110">PARAMETERS</span></span>

### <span data-ttu-id="28a51-111">-ClusterBootstrapAccountPassword</span><span class="sxs-lookup"><span data-stu-id="28a51-111">-ClusterBootstrapAccountPassword</span></span>
<span data-ttu-id="28a51-112">Password per l'account di bootstrap del cluster</span><span class="sxs-lookup"><span data-stu-id="28a51-112">Password for the cluster bootstrap account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28a51-113">-ClusterOperatorAccountPassword</span><span class="sxs-lookup"><span data-stu-id="28a51-113">-ClusterOperatorAccountPassword</span></span>
<span data-ttu-id="28a51-114">Password per l'account dell'operatore del cluster</span><span class="sxs-lookup"><span data-stu-id="28a51-114">Password for the cluster operator account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28a51-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28a51-115">-DefaultProfile</span></span>
<span data-ttu-id="28a51-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="28a51-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28a51-117">-SqlServiceAccountPassword</span><span class="sxs-lookup"><span data-stu-id="28a51-117">-SqlServiceAccountPassword</span></span>
<span data-ttu-id="28a51-118">Password per l'account SQL servizio</span><span class="sxs-lookup"><span data-stu-id="28a51-118">Password for the SQL service account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28a51-119">-SqlVM</span><span class="sxs-lookup"><span data-stu-id="28a51-119">-SqlVM</span></span>
<span data-ttu-id="28a51-120">L SQL configurazione della macchina virtuale a cui verrà aggiunta l'appartenenza ai gruppi</span><span class="sxs-lookup"><span data-stu-id="28a51-120">The SQL virtual machine configuration which group membership will be added to</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28a51-121">-SqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="28a51-121">-SqlVMGroup</span></span>
<span data-ttu-id="28a51-122">Gruppo di SQL di cui fa parte la macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="28a51-122">The group the SQL virtual machine will be part of</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28a51-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28a51-123">CommonParameters</span></span>
<span data-ttu-id="28a51-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28a51-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28a51-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="28a51-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28a51-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="28a51-126">INPUTS</span></span>

### <span data-ttu-id="28a51-127">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="28a51-127">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="28a51-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="28a51-128">OUTPUTS</span></span>

### <span data-ttu-id="28a51-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="28a51-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="28a51-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="28a51-130">NOTES</span></span>

## <span data-ttu-id="28a51-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="28a51-131">RELATED LINKS</span></span>
