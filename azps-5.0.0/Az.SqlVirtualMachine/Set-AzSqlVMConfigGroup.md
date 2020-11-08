---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/set-azsqlvmconfiggroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Set-AzSqlVMConfigGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Set-AzSqlVMConfigGroup.md
ms.openlocfilehash: b83dc58161791009a3adfd7cbf9b0b07b3f0b5b1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193599"
---
# <span data-ttu-id="d4a66-101">Set-AzSqlVMConfigGroup</span><span class="sxs-lookup"><span data-stu-id="d4a66-101">Set-AzSqlVMConfigGroup</span></span>

## <span data-ttu-id="d4a66-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d4a66-102">SYNOPSIS</span></span>
<span data-ttu-id="d4a66-103">Impostare le informazioni relative a un gruppo di macchine virtuali SQL in una configurazione di una macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="d4a66-103">Set the information relative to a sql virtual machine group in a sql virtual machine configuration.</span></span>

## <span data-ttu-id="d4a66-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d4a66-104">SYNTAX</span></span>

```
Set-AzSqlVMConfigGroup [-SqlVM] <AzureSqlVMModel> [-SqlVMGroup] <AzureSqlVMGroupModel>
 -ClusterOperatorAccountPassword <SecureString> -SqlServiceAccountPassword <SecureString>
 [-ClusterBootstrapAccountPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d4a66-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d4a66-105">DESCRIPTION</span></span>
<span data-ttu-id="d4a66-106">Il cmdlet Set-AzSqlVMConfigGroup imposta le informazioni necessarie per partecipare a un gruppo di macchine virtuali SQL per una configurazione di una macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="d4a66-106">The Set-AzSqlVMConfigGroup cmdlet set the information needed in order to join a sql virtual machine group for a sql virtual machine configuration.</span></span>

## <span data-ttu-id="d4a66-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d4a66-107">EXAMPLES</span></span>

### <span data-ttu-id="d4a66-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d4a66-108">Example 1</span></span>
```powershell
PS C:\> $config = Set-AzSqlVMConfigGroup -SqlVM $config -SqlVMGroup $group -ClusterOperatorAccountPassword 'password' -SqlServiceAccountPassword 'password'
```

<span data-ttu-id="d4a66-109">Aggiornare le informazioni di gruppo di una configurazione di una macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="d4a66-109">Update the group informations of a sql virtual machine configuration.</span></span>

## <span data-ttu-id="d4a66-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d4a66-110">PARAMETERS</span></span>

### <span data-ttu-id="d4a66-111">-ClusterBootstrapAccountPassword</span><span class="sxs-lookup"><span data-stu-id="d4a66-111">-ClusterBootstrapAccountPassword</span></span>
<span data-ttu-id="d4a66-112">Password per l'account di avvio del cluster</span><span class="sxs-lookup"><span data-stu-id="d4a66-112">Password for the cluster bootstrap account</span></span>

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

### <span data-ttu-id="d4a66-113">-ClusterOperatorAccountPassword</span><span class="sxs-lookup"><span data-stu-id="d4a66-113">-ClusterOperatorAccountPassword</span></span>
<span data-ttu-id="d4a66-114">Password per l'account operatore cluster</span><span class="sxs-lookup"><span data-stu-id="d4a66-114">Password for the cluster operator account</span></span>

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

### <span data-ttu-id="d4a66-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4a66-115">-DefaultProfile</span></span>
<span data-ttu-id="d4a66-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d4a66-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4a66-117">-SqlServiceAccountPassword</span><span class="sxs-lookup"><span data-stu-id="d4a66-117">-SqlServiceAccountPassword</span></span>
<span data-ttu-id="d4a66-118">Password per l'account del servizio SQL</span><span class="sxs-lookup"><span data-stu-id="d4a66-118">Password for the SQL service account</span></span>

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

### <span data-ttu-id="d4a66-119">-SqlVM</span><span class="sxs-lookup"><span data-stu-id="d4a66-119">-SqlVM</span></span>
<span data-ttu-id="d4a66-120">Configurazione della macchina virtuale SQL a cui verrà aggiunta l'appartenenza al gruppo</span><span class="sxs-lookup"><span data-stu-id="d4a66-120">The SQL virtual machine configuration which group membership will be added to</span></span>

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

### <span data-ttu-id="d4a66-121">-SqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="d4a66-121">-SqlVMGroup</span></span>
<span data-ttu-id="d4a66-122">Gruppo di cui la macchina virtuale SQL farà parte</span><span class="sxs-lookup"><span data-stu-id="d4a66-122">The group the SQL virtual machine will be part of</span></span>

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

### <span data-ttu-id="d4a66-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4a66-123">CommonParameters</span></span>
<span data-ttu-id="d4a66-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4a66-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4a66-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4a66-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4a66-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d4a66-126">INPUTS</span></span>

### <span data-ttu-id="d4a66-127">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="d4a66-127">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="d4a66-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d4a66-128">OUTPUTS</span></span>

### <span data-ttu-id="d4a66-129">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="d4a66-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="d4a66-130">Note</span><span class="sxs-lookup"><span data-stu-id="d4a66-130">NOTES</span></span>

## <span data-ttu-id="d4a66-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d4a66-131">RELATED LINKS</span></span>
